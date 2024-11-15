### List Incidets

```javascripts
var getCurrentCycle = Class.Create();
getCurrentCycle.prototype = Object.exendsOject(AbstractAjaxProcesser, {
  getCurrentCycleIncident: function(){
    var currentDate = new GlideDate();
    var startDate;
    var endDate;
    if(currentDate.getMonth()>=1 && currentDate.getMonth()<=6 {
      // Period
      startDate = currentDate.GetYear()+'-01-01';
      endDate = currentDate.GetYear()+'-06-30';
    } else {
      startDate = currentDate.GetYear()+'-07-31';
      endDate = currentDate.getYear()+'-12-31'

    }
    var grINC = new GlideRecord('incident');
    grINC.AddQuery('sys_created_on', '>=', startDate);
    grINC.addQuery('sys_created_on', '<=', endStart);
    grINC.query();
    while(grINC.next()){
      incArr.push(grINC.sys_id.toString());

    }
    return incArr;

    }
  },

});

```
