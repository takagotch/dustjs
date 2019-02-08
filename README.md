### dustjs
---
https://github.com/linkedin/dustjs/

```js
npm install --save --production dustjs-linkedin
npm install --global --production dustjs-linkedin

npm install --save --production dustjs-helpers
npm install --save --production dustjs-filters-secure

bower install --save dustjs-linkedin
```

```js
var compiledTemplate = dust.compile("Hello {name}!", "intro");

(function() {
  dust.register("intro", body_());
  function body_0(chk, ctx){
    return chk.write("Hello").reference(ctx._get(false, ["name"]), ctx, "h").write("!");
  }
  return body_0;
})();

var compileTemplate = dust.compile("Hello {name}!", "intro");
dust.loadSource(compiledTemplate);

dust.render("intro", {name: "Fred"}, function(error, output){
  if(err){
    console.log(error);
  } else {
    console.log(ouput);
  }
});

var stream = dust.stream(templateName, data);
stream.on('data', dataCallback)
  .on('end', endCallback)
  .on('error', errorCallback);
  
var output, finished;
dust.stream(test.name, context)
  .on('data', function(segment){
    output += segment;
  }).on('end', function(){
    finished = true;
    console.log(output);
  }).on('error', function(error){
    finished = true;
    output = error.message || error;
    console.log(output);
  });
  
dust.helpers.myHelper = function(chunk, context, bodies, params){
  return chunk;
}

dust.helpers.period = function(chunk, context, bodies, params){
  var location = params.location,
    body = bodies.block;
  if(location === 'start'){
    chunk.write('.');
    chunk.write('.');
  } else if (location === 'end'){
    chunk.render(body, context);
    chunk.write('.');
  } else {
    dust.log('WARN', 'missing parameter "location" in period helper');
  }
  return chunk;
};
```

```
```

