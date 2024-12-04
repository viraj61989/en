// Convert a color's Hex code to RGB.
function hexToRgb(hex) {
    var result = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(hex);
    return result ? {
        r: parseInt(result[1], 16),
        g: parseInt(result[2], 16),
        b: parseInt(result[3], 16)
    } : null;
}

// Define our CSS customization rules.
var customCSS = {
    'page': {
        'attributes': {
            'background': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['page']['background']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['page']['background']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['page']['background']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['page']['background']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker-background',
                'title': 'Background',
                'type': 'background'
            },
            'opacity': {
                'attribute': 'opacity',
                'custom': '{{opacity}}',
                'customVars': {
                    'opacity': function() {
                        return parseInt(useLockerSettings['css']['pc']['page']['opacity']) / 100;
                    }
                },
                'devices': ['pc'],
                'element': '#my-locker-background',
                'range': [0, 100],
                'title': 'Opacity',
                'type': 'range'
            }
        },
        'title': 'Page',
        'type': 'group'
    },
    'locker': {
        'attributes': {
            'font': {
                'attribute': 'font-family',
                'custom': "'{{value}}', sans-serif !important",
                'devices': ['pc'],
                'element': '#my-locker',
                'options': [
                    {
                        'title': 'Montserrat',
                        'value': 'Montserrat'
                    },
                    {
                        'title': 'Open Sans',
                        'value': 'Open Sans'
                    },
                    {
                        'title': 'Roboto',
                        'value': 'Roboto'
                    },
                    {
                        'title': 'Arial',
                        'value': 'Arial'
                    },
                    {
                        'title': 'Verdana',
                        'value': 'Verdana'
                    }
                ],
                'title': 'Font',
                'type': 'options'
            },
            'box-shadow': {
                'attribute': 'box-shadow',
                'custom': '0px 1px 22px {{rgb}}',
                'customVars': {
                    'rgb': function() {
                        // What's the current value?
                        var currentValue = useLockerSettings['css']['pc']['locker']['box-shadow'];

                        // What value do we return?
                        var returnValue = 'transparent';

                        // If the value isn't "transparent".
                        if (currentValue != 'transparent') {
                            // Take the current value and convert it to RGB.
                            var rgb = hexToRgb(currentValue);

                            // Return our string.
                            returnValue = 'rgba('+rgb.r +', '+rgb.g+', '+rgb.b+', 0.56)';
                        }

                        // Return our value.
                        return returnValue;
                    }
                },
                'devices': ['pc'],
                'element': '#my-locker',
                'title': 'Border Shadow Color',
                'type': 'color'
            },
            'border-radius': {
                'attribute': 'border-radius',
                'custom': '{{value}}px',
                'devices': ['pc'],
                'element': '#my-locker',
                'range': [0, 10],
                'title': 'Border Radius',
                'type': 'range'
            },
            'width': {
                'attribute': 'max-width',
                'custom': '{{value}}px',
                'devices': ['pc'],
                'element': '#my-locker',
                'range': [500, 1000],
                'title': 'Width',
                'type': 'range'
            }
        },
        'title': 'Content Locker',
        'type': 'group'
    },
    'header': {
        'attributes': {
            'display': {
                'attribute': 'display',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-top',
                'options': [
                    {
                        'title': 'Visible',
                        'value': 'block'
                    },
                    {
                        'title': 'Hidden',
                        'value': 'none'
                    }
                ],
                'title': 'Visibility',
                'type': 'options'
            },
            'background': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['header']['background']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['header']['background']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['header']['background']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['header']['background']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-top',
                'title': 'Background',
                'type': 'background'
            },
            'border-color': {
                'attribute': 'border-bottom-color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-top',
                'title': 'Border Color',
                'type': 'color'
            },
            'border-width': {
                'attribute': 'border-bottom-width',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-top',
                'range': [0, 5],
                'title': 'Border Width',
                'type': 'range'
            },
            'border-box-shadow': {
                'attribute': 'box-shadow',
                'custom': '0px 2px 5px {{value}}',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-top',
                'title': 'Border Shadow Color',
                'type': 'color'
            },
            'padding-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-top',
                'range': [0, 250],
                'title': 'Padding Top',
                'type': 'range'
            },
            'padding-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-top',
                'range': [0, 250],
                'title': 'Padding Bottom',
                'type': 'range'
            },
            'font-align': {
                'attribute': 'text-align',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-top span',
                'options': [
                    {
                        'title': 'Center',
                        'value': 'center'
                    },
                    {
                        'title': 'Left',
                        'value': 'left'
                    },
                     {
                        'title': 'Right',
                        'value': 'right'
                    }
                ],
                'title': 'Text Alignment',
                'type': 'options'
            },
            'font-color': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-top span',
                'title': 'Text Color',
                'type': 'color'
            },
            'font-size': {
                'attribute': 'font-size',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-top span',
                'range': [12, 20],
                'title': 'Text Size',
                'type': 'range'
            },
            'font-weight': {
                'attribute': 'font-weight',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-top span',
                'options': [
                    {
                        'title': 'Normal',
                        'value': 'normal'
                    },
                    {
                        'title': 'Bold',
                        'value': 'bold'
                    }
                ],
                'title': 'Text Weight',
                'type': 'options'
            }
        },
        'title': 'Header',
        'type': 'group'
    },
    'body': {
        'attributes': {
            'background': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['body']['background']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['body']['background']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['body']['background']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['body']['background']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body',
                'title': 'Background',
                'type': 'background'
            }
        },
        'title': 'Body',
        'type': 'group'
    },
    'body-human-verification': {
        'attributes': {
            'background': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'title': 'Background',
                'type': 'background'
            },
            'background-hover': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background-hover']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background-hover']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background-hover']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['body-human-verification']['background-hover']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button:hover',
                'title': 'Background (Hover)',
                'type': 'background'
            },
            'border-radius': {
                'attribute': 'border-radius',
                'custom': '{{value}}px',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'range': [0, 15],
                'title': 'Border Radius',
                'type': 'range'
            },
            'border-color': {
                'attribute': 'border-color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'title': 'Border Color',
                'type': 'color'
            },
            'border-color-hover': {
                'attribute': 'border-color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button:hover',
                'title': 'Border Color (Hover)',
                'type': 'color'
            },
            'border-width': {
                'attribute': 'border-width',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'range': [0, 5],
                'title': 'Border Width',
                'type': 'range'
            },
            'font-size': {
                'attribute': 'font-size',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'range': [8, 25],
                'title': 'Text Size',
                'type': 'range'
            },
            'font-weight': {
                'attribute': 'font-weight',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'options': [
                    {
                        'title': 'Normal',
                        'value': 'normal'
                    },
                    {
                        'title': 'Bold',
                        'value': 'bold'
                    }
                ],
                'title': 'Text Weight',
                'type': 'options'
            },
            'font-color': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'title': 'Text Color',
                'type': 'color'
            },
            'font-color-hover': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-human-verification button:hover',
                'title': 'Text Color (Hover)',
                'type': 'color'
            },
            'padding-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'range': [0, 250],
                'title': 'Padding Top',
                'type': 'range'
            },
            'padding-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification button',
                'range': [0, 250],
                'title': 'Padding Bottom',
                'type': 'range'
            },
            'margin-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification',
                'range': [0, 250],
                'title': 'Margin Top',
                'type': 'range'
            },
            'margin-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-human-verification',
                'range': [0, 250],
                'title': 'Margin Bottom',
                'type': 'range'
            }
        },
        'title': 'Body > Human Verification',
        'toggle-span': {
            'elements': [
                '#my-locker-body-offers',
                '#my-locker-body-human-verification'
            ],
            'start': (useLockerSettings['other']['human-verification'] == 'enabled' ? 'Hide' : 'Show')
        },
        'type': 'group'
    },
    'body-offers': {
        'attributes': {
            'text-top-align': {
                'attribute': 'text-align',
                'devices': ['pc'],
                'element': '#my-locker .my-locker-body-text-top',
                'options': [
                    {
                        'title': 'Center',
                        'value': 'center'
                    },
                    {
                        'title': 'Left',
                        'value': 'left'
                    },
                     {
                        'title': 'Right',
                        'value': 'right'
                    }
                ],
                'title': 'Top Text Alignment',
                'type': 'options'
            },
            'text-top-color': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker .my-locker-body-text-top',
                'title': 'Top Text Color',
                'type': 'color'
            },
            'text-top-size': {
                'attribute': 'font-size',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-top',
                'range': [10, 25],
                'title': 'Top Text Size',
                'type': 'range'
            },
            'text-top-weight': {
                'attribute': 'font-weight',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-top',
                'options': [
                    {
                        'title': 'Normal',
                        'value': 'normal'
                    },
                    {
                        'title': 'Bold',
                        'value': 'bold'
                    }
                ],
                'title': 'Top Text Weight',
                'type': 'options'
            },
            'text-top-shadow': {
                'attribute': 'text-shadow',
                'custom': '1px 1px 2px {{value}}',
                'devices': ['pc'],
                'element': '#my-locker .my-locker-body-text-top',
                'title': 'Top Text Shadow Color',
                'type': 'color'
            },
            'text-top-padding-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-top',
                'range': [0, 250],
                'title': 'Top Text Padding Top',
                'type': 'range'
            },
            'text-top-padding-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-top',
                'range': [0, 250],
                'title': 'Top Text Padding Bottom',
                'type': 'range'
            },
            'text-bottom-align': {
                'attribute': 'text-align',
                'devices': ['pc'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'options': [
                    {
                        'title': 'Center',
                        'value': 'center'
                    },
                    {
                        'title': 'Left',
                        'value': 'left'
                    },
                     {
                        'title': 'Right',
                        'value': 'right'
                    }
                ],
                'title': 'Bottom Text Alignment',
                'type': 'options'
            },
            'text-bottom-color': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'title': 'Bottom Text Color',
                'type': 'color'
            },
            'text-bottom-size': {
                'attribute': 'font-size',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'range': [10, 25],
                'title': 'Bottom Text Size',
                'type': 'range'
            },
            'text-bottom-weight': {
                'attribute': 'font-weight',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'options': [
                    {
                        'title': 'Normal',
                        'value': 'normal'
                    },
                    {
                        'title': 'Bold',
                        'value': 'bold'
                    }
                ],
                'title': 'Bottom Text Weight',
                'type': 'options'
            },
            'text-bottom-shadow': {
                'attribute': 'text-shadow',
                'custom': '1px 1px 2px {{value}}',
                'devices': ['pc'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'title': 'Bottom Text Shadow Color',
                'type': 'color'
            },
            'text-bottom-padding-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'range': [0, 250],
                'title': 'Bottom Text Padding Top',
                'type': 'range'
            },
            'text-bottom-padding-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker .my-locker-body-text-bottom',
                'range': [0, 250],
                'title': 'Bottom Text Padding Bottom',
                'type': 'range'
            }
        },
        'title': 'Body > Offers',
        'type': 'group'
    },
    'body-offers-list': {
        'attributes': {
            'align': {
                'attribute': 'text-align',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'options': [
                    {
                        'title': 'Center',
                        'value': 'center'
                    },
                    {
                        'title': 'Left',
                        'value': 'left'
                    },
                     {
                        'title': 'Right',
                        'value': 'right'
                    }
                ],
                'title': 'Alignment',
                'type': 'options'
            },
            'width': {
                'attribute': 'width',
                'custom': '{{value}}%',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [50, 100],
                'title': 'Width (Percentage)',
                'type': 'range'
            },
            'background': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'title': 'Background',
                'type': 'background'
            },
            'background-hover': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background-hover']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background-hover']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background-hover']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['body-offers-list']['background-hover']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a:hover',
                'title': 'Background (Hover)',
                'type': 'background'
            },
            'border-radius': {
                'attribute': 'border-radius',
                'custom': '{{value}}px',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [0, 15],
                'title': 'Border Radius',
                'type': 'range'
            },
            'border-color': {
                'attribute': 'border-color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'title': 'Border Color',
                'type': 'color'
            },
            'border-width': {
                'attribute': 'border-width',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [0, 5],
                'title': 'Border Width',
                'type': 'range'
            },
            'text-align': {
                'attribute': 'text-align',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'options': [
                    {
                        'title': 'Center',
                        'value': 'center'
                    },
                    {
                        'title': 'Left',
                        'value': 'left'
                    },
                     {
                        'title': 'Right',
                        'value': 'right'
                    }
                ],
                'title': 'Text Alignment',
                'type': 'options'
            },
            'font-size': {
                'attribute': 'font-size',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [8, 25],
                'title': 'Text Size',
                'type': 'range'
            },
            'font-weight': {
                'attribute': 'font-weight',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'options': [
                    {
                        'title': 'Normal',
                        'value': 'normal'
                    },
                    {
                        'title': 'Bold',
                        'value': 'bold'
                    }
                ],
                'title': 'Text Weight',
                'type': 'options'
            },
            'font-color': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'title': 'Text Color',
                'type': 'color'
            },
            'font-color-hover': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a:hover',
                'title': 'Text Color (Hover)',
                'type': 'color'
            },
            'margin-top': {
                'attribute': 'margin-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [0, 250],
                'title': 'Margin Top',
                'type': 'range'
            },
            'margin-bottom': {
                'attribute': 'margin-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [0, 250],
                'title': 'Margin Bottom',
                'type': 'range'
            },
            'padding-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [0, 250],
                'title': 'Padding Top',
                'type': 'range'
            },
            'padding-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-body-offers #my-locker-body-offers-list a',
                'range': [0, 250],
                'title': 'Padding Bottom',
                'type': 'range'
            }
        },
        'title': 'Body > Offers > Offer List',
        'type': 'group'
    },
    'footer': {
        'attributes': {
            'display': {
                'attribute': 'display',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-bottom',
                'options': [
                    {
                        'title': 'Visible',
                        'value': 'block'
                    },
                    {
                        'title': 'Hidden',
                        'value': 'none'
                    }
                ],
                'title': 'Visibility',
                'type': 'options'
            },
            'background': {
                'attribute': 'background',
                'custom': 'url({{image}}) {{vertical}} {{horizontal}} no-repeat {{color}}',
                'customVars': {
                    'color': function() {
                        return useLockerSettings['css']['pc']['footer']['background']['color'];
                    },
                    'horizontal': function() {
                        return useLockerSettings['css']['pc']['footer']['background']['horizontal'];
                    },
                    'image': function() {
                        return useLockerSettings['css']['pc']['footer']['background']['image'];
                    },
                    'vertical': function() {
                        return useLockerSettings['css']['pc']['footer']['background']['vertical'];
                    },
                },
                'devices': ['pc'],
                'element': '#my-locker #my-locker-bottom',
                'title': 'Background',
                'type': 'background'
            },
            'border-color': {
                'attribute': 'border-top-color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-bottom',
                'title': 'Border Color',
                'type': 'color'
            },
            'border-width': {
                'attribute': 'border-top-width',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-bottom',
                'range': [0, 5],
                'title': 'Border Width',
                'type': 'range'
            },
            'border-box-shadow': {
                'attribute': 'box-shadow',
                'custom': '0px -2px 5px {{value}}',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-bottom',
                'title': 'Border Shadow Color',
                'type': 'color'
            },
            'padding-top': {
                'attribute': 'padding-top',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-bottom',
                'range': [0, 250],
                'title': 'Padding Top',
                'type': 'range'
            },
            'padding-bottom': {
                'attribute': 'padding-bottom',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-bottom',
                'range': [0, 250],
                'title': 'Padding Bottom',
                'type': 'range'
            },
            'font-align': {
                'attribute': 'text-align',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-bottom span',
                'options': [
                    {
                        'title': 'Center',
                        'value': 'center'
                    },
                    {
                        'title': 'Left',
                        'value': 'left'
                    },
                     {
                        'title': 'Right',
                        'value': 'right'
                    }
                ],
                'title': 'Text Alignment',
                'type': 'options'
            },
            'font-color': {
                'attribute': 'color',
                'devices': ['pc'],
                'element': '#my-locker #my-locker-bottom span',
                'title': 'Text Color',
                'type': 'color'
            },
            'font-size': {
                'attribute': 'font-size',
                'custom': '{{value}}px',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-bottom span',
                'range': [9, 14],
                'title': 'Text Size',
                'type': 'range'
            },
            'font-weight': {
                'attribute': 'font-weight',
                'devices': ['pc', 'phone'],
                'element': '#my-locker #my-locker-bottom span',
                'options': [
                    {
                        'title': 'Normal',
                        'value': 'normal'
                    },
                    {
                        'title': 'Bold',
                        'value': 'bold'
                    }
                ],
                'title': 'Text Weight',
                'type': 'options'
            }
        },
        'title': 'Footer',
        'type': 'group'
    }
};

// Apply our Locker Settings.
function applyLockerSettings() {
    // Define a function to replace some text with functions.
    var makeTextReplacements = function(text) {
        // Dots.
        text = text.replace('%dots%', '<span class="live-dots">.</span>');

        return text;
    };

    // When the Human Verification button is clicked.
    $('#my-locker #my-locker-body-human-verification button')
        .off('click')
        .on('click', function() {
            $('#my-locker-body-human-verification').hide();
            $('#my-locker-body-offers').show();
        });

    // Set the appropriate text.
    $('#my-locker #my-locker-top span').html(makeTextReplacements(useLockerSettings['text']['header']));
    $('#my-locker #my-locker-bottom span').html(makeTextReplacements(useLockerSettings['text']['footer']));
    $('#my-locker .my-locker-body-text-top').html(makeTextReplacements(useLockerSettings['text']['body-top']));
    $('#my-locker .my-locker-body-text-bottom').html(makeTextReplacements(useLockerSettings['text']['body-bottom']));
    $('#my-locker #my-locker-body-human-verification button')
        .html('<i class="fa fa-spinner fa-spin"></i>' +
              makeTextReplacements(useLockerSettings['text']['human-verification']));

    // Remove the "hidden" class from all Offers.
    $('#my-locker-body-offers-list a').removeClass('hidden');

    // Apply the "hidden" class to the Offers that need it.
    $('#my-locker-body-offers-list a:gt('+(parseInt(useLockerSettings['offers']['display']) - 1)+')').addClass('hidden');

    // How are we aligning the Offer links?
    $('#my-locker-body-offers-list').attr('align', useLockerSettings['css']['pc']['body-offers-list']['align']);

    // Determine what Device is being looked at.
    var device = $('#my-customization-treeview').data('device');

    // Hide all device-dependent items.
    $('#my-customization-treeview .device-dependent').hide();

    // Show all device-dependent items using this device.
    $('#my-customization-treeview .device-dependent.device-'+device).show();

    // Add this device class to our <BODY>
    $('body').removeClass('device-pc device-phone').addClass('device-'+device);

    // If they're editing, manipulate the mobile class.
    if (editing === true) {
        $('body').removeClass('mobile');

        // If the mobile device was chosen.
        if (device == 'phone') {
            $('body').addClass('mobile');
        }
    }

    // Locate the existing custom style.
    var $style = $('style#my-locker-css');

    // If this style exists, remove it.
    if ($style.length == 1) {
        $style.remove();
    }

    // What CSS rules should be applied?
    var cssRules = [];

    var createRecursiveCSSRules = function(device, mainSection, attributes) {
        // Loop through all attributes.
        $.each(attributes, function(type, data) {
            // If this is a group.
            if (data.type == 'group') {
                createRecursiveCSSRules(device, (mainSection === null ? type : mainSection), data.attributes);
            }
            // If there's an attribute to set.
            else if ('attribute' in data && 'element' in data && type in useLockerSettings['css'][device][mainSection]) {
                // What's the value for this attribute?
                var value = useLockerSettings['css'][device][mainSection][type] || '';

                // What CSS string do we add?
                var cssString = data.element+' { '+data.attribute+': '+value+'; }';

                // Do we need to do any custom stuff to it?
                if ('custom' in data) {
                    // Set the CSS string we'll be appending.
                    cssString = data.element+' { '+data.attribute+': '+data.custom.replace('{{value}}', value)+'; }';

                    // If there are any more custom variables we need to replace.
                    if ('customVars' in data) {
                        $.each(data.customVars, function(customKey, customValue) {
                            cssString = cssString.replace('{{'+customKey+'}}', customValue);
                        });
                    }
                }

                // If this is for Mobile Phones.
                if (device == 'phone') {
                    cssString = 'body.mobile '+cssString;
                }

                // Append our rule.
                cssRules.push(cssString);
            }
        });
    };

    // If we're using the default settings.
    $.each(['pc', 'phone'], function(deviceIndex, device) {
        createRecursiveCSSRules(device, null, customCSS);
    });

    // Append the mobile rules.
    cssRules.push('body.mobile #my-locker { margin: 2% auto 0 !important; width: 95% !important; }');
    cssRules.push('body.device-phone #my-locker { margin: 39px 0 0 380px !important; width: 480px !important; }');

    // Retrieve the CSS rules.
    $('<style id="my-locker-css">'+cssRules.join(' ')+'</style>').insertBefore('#my-locker');

    // Take care of our Custom CSS.
    $('style#my-custom-css').remove();

    // Apply their Custom CSS.
    $('<style id="my-custom-css">'+useLockerSettings['css-custom']+'</style>').insertAfter('style#my-locker-css');

     // Take care of our Custom JavaScript.
    $('script#my-custom-javascript').remove();

    // Apply their Custom JavaScript.
    $('<script id="my-custom-javascript">'+useLockerSettings['javascript-custom']+'</script>').insertAfter('style#my-locker-css');
}

// Set the live dots text.
$('.live-dots').text('.');

// Determine whether we're using Mobile or not, based on size.
var isMobileSize = function() {
    // If editing is enabled.
    if (editing === false) {
        // Locate our <BODY> element.
        var $body = $('body');

        // If the body exists.
        if ($body.length == 1) {
            // What is the current body width?
            var bodyWidth = $body.innerWidth();

            // If the width is a number, and is greater than 0.
            if (!isNaN(bodyWidth) && bodyWidth > 0) {
                // What is the width to determine if it's Mobile?
                var mobileWidth = 500;

                // If this isn't Mobile.
                if (bodyWidth > mobileWidth) {
                    $body.removeClass('mobile');
                }
                else {
                    $body.addClass('mobile');
                }
            }
        }
    }
};

// Check the body size.
isMobileSize();

// When the page is loaded, show the Content Locker.
$(document).ready(function() {
    // Check the body size.
    isMobileSize();

    /*
    // When the window size is changed.
    $(window).resize(function() {
        isMobileSize();
    });
    */

    // If Human Verification is enabled.
    if (useLockerSettings['other']['human-verification'] == 'enabled') {
        $('#my-locker-body-human-verification').show();
        $('#my-locker-body-offers').hide();
    }

    // An array of HTML elements.
    var html = [];

    // If the Offers was provided as a string, convert it.
    if (typeof userOffers == 'string') {
        useOffers = JSON.parse(useOffers);
    }

    // Loop through each Offer and generate its HTML.
    $.each(useOffers, function(index, offer) {
        html
            .push('<a href="'+offer.url+'" class="notranslate offerURL '+((index + 1) > useLockerSettings['offers']['display'] ? 'hidden' : '')+'" ' +
                        'target="_blank" data-payout="'+offer.user_payout+'" title="'+offer.conversion+'">' +
                        '<span>'+offer.anchor+'</span>' +
                  '</a>');
    });

    // Add the Offers to the list.
    $('#my-locker-body-offers-list').append(html.join(''));

    // Apply the Settings.
    applyLockerSettings();

    // Show the Content Locker.
    $('#my-locker').show();

    $('body').data('dots', 1);

    // Have the dots alternate.
    setInterval(function() {
        // How many dots are displayed?
        var dots = parseInt($('body').data('dots'));

        // How many dots should be shown?
        var showDots = (dots == 3 ? 1 : dots + 1);

        // Set the dot string.
        var dotString = '';

        // Set the dots.
        for(var i = 1; i <= showDots; i++) {
            dotString += '.';
        }

        // Set the dot string.
        $('.live-dots').text(dotString);

        // Set how many dots there are.
        $('body').data('dots', showDots);
    }, 750);
});

// Listen for orientation changes
window.addEventListener('orientationchange', function() {
    isMobileSize();
}, false);

// Listen for resize changes
window.addEventListener('resize', function() {
    isMobileSize();
}, false);