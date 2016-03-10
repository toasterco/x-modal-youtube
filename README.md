## &lt;swiper-behavior&gt;

**Polymer** element. Use `<x-modal-youtube>` to open any youtube video in a
modal dialog just by firing the `x-modal-youtube-open` iron-signal.

Use neon animations to change the way the dialog appears/disappears. You can
either use the shorthand `entry-animation` and `exit-animation` properties,
or specify the detailed configuration object via the `animationConfig` attribute.

Example:



    <link rel="import" href="components/neon-animation/animations/fade-in-animation.html">
    <link rel="import" href="components/neon-animation/animations/fade-out-animation.html">

    ...

    <x-modal-youtube
        entry-animation="fade-in-animation"
        exit-animation="fade-out-animation"></x-modal-youtube>


For best results, add this element directly in the document's `<body>`.

You can open the dialog by firing the `x-modal-youtube-open` event:

    this.fire('iron-signal', {
      name: 'x-modal-youtube-open',
      data: {
        youtubeId: '...'
      }
    });


Alternatively:

- the `youtubeId` attribute can be used to change the video.

- the `open()`, `close()`, and `toogle()` methods can be used to control the dialog.



### Styling

The following custom properties and mixins are available for styling.

Custom property | Description | Default
----------------|-------------|----------
`--x-modal-youtube-max-video-width` | Max width fot the YouTube video             | `1000px`
`--x-modal-youtube-spinner-color`   | Color of the spinner                        | `white`
`--x-modal-youtube-dismiss-button`  | Mixin applied to the dismiss button (cross) | `{}`


The backdrop element's background color and opacity can be changed via the
`--iron-overlay-backdrop-background-color` and `--iron-overlay-backdrop-opacity`
CSS properties. They should be set in the page root, since the `<iron-overlay-backdrop>`
element will get appended to the document's `<body>`.


## Install

`bower install --save x-modal-youtube`