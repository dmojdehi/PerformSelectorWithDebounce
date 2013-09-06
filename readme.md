


PerformSelectorWithDebounce
---------------------------


A simple way to throttle messages spammed to an object.  

This commonly happens when updating the UI from a event that may fire frequently.  



For example, the handler for the 'value changed' event from a slider may be called extremely frequently.


	- (IBAction)mySliderValueChanged
	{
		[self updateUI];
	}


Rather than update your UI 100 times per second, 10 times per second is perfectly adequate:
	
	#import "PerformSelectorWithDebounce.h"

	- (IBAction)mySliderValueChanged
	{
		[self performSelector:@selector(updateUI) withDebounceDuration:0.1];
	}




License: MIT

