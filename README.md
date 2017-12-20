# hello-world
我的第一个github项目
$("select[name=seatLevel]").change(function(){
		var val = $(this).find('option:selected').text();
		var seatType_sel = $("select[name=seatType]");
		seatType_sel.find("option").hide();
		seatType_sel.find("option").prop('selected',false);
		seatType_sel.find("option:contains("+val+")").show();
		if(val == '商务舱'){
			seatType_sel.find("option:contains(\"公务舱\")").show();
		}
		$(seatType_sel.find("option:contains("+val+")")[0]).prop('selected',true);
	});
