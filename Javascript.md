###Object Construction

<pre>
// literal construction
var james = {
    // add properties to this object!
    job: "programmer",
    married: false
};

// constructor construction
function Person(job, married) {
    this.job = job;
    this.married = married;
}

// create a "gabby" object using the Person constructor!
var gabby = new Person("student", true);
</pre>
