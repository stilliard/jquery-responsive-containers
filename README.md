
jQuery Responsive Containers (Also known as selector queries)
===============================================================

# UPDATE: This plugin is no longer maintained, please use [EQCSS](https://github.com/eqcss/eqcss) instead or the fantastic new [Container Queries available in CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries).

We have media queries, hooray, but what about a way to pass modules around and have them respond / adapt to where the person puts them on a page, what if there added to a large space, or a small sidebar. And in turn, what happens when that page responds and elements around it change causing its container width to change?
Well, this plugin was a quick way to hopefully solve that problem for a temp basis.
Why only temp? because i hope the CSS working group will work out a better CSS implementation at some point, it really is needed if web app mashups are to be responsive.

This plugin is very simple in what it does, and mainly wraps the jquery-resize plugin with a nice way to use it to make responsive containers.

The end jquery.responsive-containers.min.js contains both the jquery-responsive-containers plugin and the jquery-resize plugin for simplicity, but you can easily split them out if needed.

Demo's coming soon! For now there is a demo in the code so if you checkout the latest code and run firefox ./demo/index.html you can have a quick play.

Examples
---------
Min width with a class name addition

    $('.myModule').responsiveContainer({
        feature: 'min-width',
        value: '800px',
        className: 'myModule-large'
    });

Max width with a class name addition

    $('.myModule').responsiveContainer({
        feature: 'max-width',
        value: '400px',
        className: 'myModule-small'
    });

Max width with a custom callback

    $('.myModule').responsiveContainer({
        feature: 'max-width',
        value: '400px',
        callback: function (data) {
            console.log(data);
        }
    });


Credits
---------

[jQuery](http://jquery.com/)

[jquery-resize](https://github.com/cowboy/jquery-resize)

Inspired somewhat by Andy Humes article on [Responsive Containers](http://blog.andyhume.net/responsive-containers/)



[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/stilliard/jquery-responsive-containers/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

