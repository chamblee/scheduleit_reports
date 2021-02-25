# Schedule It Reports

Custom reporting templates for the resource-scheduling software Schedule It (Desktop/On-Premises Version).
#
The out-of-the-box reporting tools in Schedule It were not fully meeting the client's needs. 

My solution was to extend Schedule It's native reporting options by using HTML with internal CSS and JavaScript as a report template (The CSS and JS is internal because the client wanted self-contained templates that could be easily exchanged amongst their Schedule It users).

#
## Schedule It Data Tags

These reports use Schedule It's native data tags for custom reporting... specifically for the Desktop/On-Premises version of Schedule It. There may be some differeneces in the data tags if you are using the cloud version.

[Schedule It Data Tag Documentation](https://www.scheduleit.com/faq/10055/customise-the-desktop-reports-templates-and-change-the-tags)

#
## How to Use:
Change any data tags as needed to match with your Schedule It resource names, groups, and/or custom data fields.

Below is an example showing the use of Schedule It data tags (with prefix SI-).

This example captures the event loop from Schedule It and assigns each event's properties to a new training event object and stores them in an array.

```
let events = [];

function trainingEvent(title, date, duration, resources, instructors, project) {
    this.title = title;
    this.date = new Date(date);
    this.duration = duration;
    this.resources = resources;
    this.instructors = instructors;
    this.project = project;
}

SI-EventLoop
	events.push(new trainingEvent(
            "SI-E-Title", 
            "SI-E-ShortDateStart", 
            parseFloat("SI-E-DurationH"), 
            "SI-E-OwnersNamesAll",
            "SI-E-NamesIn-816-Group",
            "SI-E-Custom1"
        );
	);
SI-EventLoopEnd
```


#
## License:

[MIT](https://choosealicense.com/licenses/mit/)


------------------------------------------------------

