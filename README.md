# Test exan on frontend developer vacancy

## The guidance for the test task.
For resolving the task it is allowed and necessary to use any frameworks and components which would save yopur time and allow to solve the task optimally. However, we ask you to provide short description of frameworks or libraries were used and what for.


## Refactoring

Task to review and improve existing code.

Please review code below:

```javascript
function func(s, a, b) {

	if (s.match(/^$/)) {
		return -1;
	}
	
	var i = s.length -1;
	var aIndex =     -1;
	var bIndex =     -1;
	
	while ((aIndex == -1) && (bIndex == -1) && (i > 0)) {
	    if (s.substring(i, i +1) == a) {
	    	aIndex = i;
    	}
	    if (s.substring(i, i +1) == b) {
	    	bIndex = i;
    	}
	    i = i - 1;
	}
	
	if (aIndex != -1) {
	    if (bIndex == -1) {
	        return aIndex;
	    }
	    else {
	        return Math.max(aIndex, bIndex);
	    }
	}
	
	if (bIndex != -1) {
	    return bIndex;
	}
	else {
	    return -1;
	}
}
```

What can be improved here? How would you re-write it?


## Practical test

 - We dont have full detailed requirements to the system functionality here as they are not necessary in this task and you are allowed to make certain assumptions. The purpose of this task is to assess your practice skills of developing and designing the client part of web applications.
 - All calls to the API / server-side must be mocked.
 - We dont provide design of the screens here, so the level of design / pixel perfect layout will not be evaluated here.
 - The layout of all screens must be adaptive - to support different sizes of device screens, including mobile screens.

### Payment terminal for the cell providers 

Develop (HTML/CSS-coding and implement client-side logic) application interface for the terminal providing the service of refilling the balance of cellular operators. The application should have the following screens / basic input and control elements:

1. Main screen
 - The list of supported telecom operators: MTS, Beeline, Megafon (implement flexibility to extend list of supported operators).
 - Click on certain operator should redirec to the refilling screen.
2. Refill balance form
 - Identifier of the selected operator
 - Phone number input field (with mask and validation)
 - The field for entering the amount of refill in rubles (with mask and validation, min possible amount - 1 rub, max - 1000 rubles)
 - Submit button - should wait for a response from the server, show a message about the success or error. In case of success, return to the main screen. Success and error should be implemented randomly.
 

## Comments

The result of your work should be published here, on github. You should send us link to github repository with source code and a link to the working version of the app (for this you can use github pages or any other hosting).

If you have questions, you can always ask them by contacting the person who gave you the task.
