var timeout; // jQ mobile kludge to prevent double-calling

$(document).ready(function()
{
	$('#countdown').each(function(i, e)
	{
		if(timeout) return;
		var downloadbtn = $(e).parent().find('.downloadbtn');
		$(downloadbtn).attr('disabled', false);
		timeout = setTimeout(tick, 1000);

		function tick()
		{
			console.log('Tick');
			var remaining = parseInt($(e).find(".seconds").text()) - 1;
			if(remaining <= 0)
			{
				$(e).css('visibility', 'hidden');
				$('.downloadbtn').attr('disabled', false);
			}
			else
			{
				$(e).css('visibility', 'hidden');
				$('.downloadbtn').attr('disabled', false);
			}
		}
	});
});
