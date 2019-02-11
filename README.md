# webpack_sass_gulp
boilerplate för gulp och sass och webpack 

clona och använd.
kör

1. npm init

2. npm install --save-dev gulp gulp-sass gulp-autoprefixer gulp-rename gulp-clean-css gulp-sourcemaps webpack-stream

3. npm i -g gulp-cli

4. npm install gulp -g --save

5. npm install jquery --save


glöm inte att lägga till .gitignore (med texten:node_modules/) i "node_modules" foldern så att inte alla dependencyfilerna kommer med i gitt repot.

In gulp 3.x you could just pass the name of a task to gulp.watch() like this:

gulp.task('watch', function() {
  gulp.watch('app/css/*.css', ['styles']);
  gulp.watch('app/js/*.js', ['scripts']);
  gulp.watch('app/img/*', ['images']);
});
In gulp 4.x this is no longer the case. You have to pass a function. The customary way of doing this in gulp 4.x is to pass a gulp.series() invocation with only one task name. This returns a function that only executes the specified task:

gulp.task('watch', function() {
  gulp.watch('app/css/*.css', gulp.series('styles'));
  gulp.watch('app/js/*.js', gulp.series('scripts'));
  gulp.watch('app/img/*', gulp.series('images'));
});
