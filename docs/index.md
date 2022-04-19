BALL UI Components
===

All the form components have the following properties common:

Property | Default Value| Required?
:------------ | :------------- | :------------
name | None | Yes
label | Empty String  | No
value| Empty String| No. Depends on required property
helpText| Empty String | No
placeholder| Empty String | No
prepend| Empty String | No
append| Empty String | No
leftCol| col-sm-3 | No
rightCol| col-sm-3 | No
align| text-md-right | No
required| false | No

---------------------
Form Base
---

Wraps one or more form fields know as form components. with an action button which allows form data to be submitted.

```php
@component('components.themes.default.form-base', [
    'action' => route('$action$'),
    'form' => '$form$',
    'method' => '$method$',
    '$model$' => $$$model$
])
    <button type="submit" class="btn btn-primary btn-block">Add</button>
@endcomponent
```

Property | Default Value| Required?
:------------ | :------------- | :------------
action | Empty. any plain url or route() | No
form | Empty. path to blade component containing form components | Yes
method| POST. Accepts GET, POST| No

---

Input
---
```php
@component('components.themes.default.input',[
    'type' => '$TEXT$',
    'label' => '$LABEL$',
    'name' => '$NAME$',
    'value' => $VALUE$->$NAME$,
    'helpText' => '$HELPTEXT$',
    'placeholder' => '$PLACEHOLDER$',
    'prepend' => '$PREPEND$',
    'append' => '$APPEND$',
    'leftCol'        => '$leftCol$',
    'rightCol'       => '$rightCol$',
])@endcomponent
```

---

Textarea
---
```php
@component('components.themes.default.textarea',[
    'label' => '$LABEL$',
    'name' => '$NAME$',
    'value' => $VALUE$->$NAME$,
    'helpText' => '$HELPTEXT$'
])@endcomponent
```
---

CheckBox
---

```php
@component('components.themes.default.checkbox',[
    'label' => '$LABEL$',
    'name' => '$NAME$',
    'value' => $VALUE$->$NAME$,
    'helpText' => '$HELPTEXT$',
    'placeholder' => '$PLACEHOLDER$',
])@endcomponent
```

---

Radio
---
```php
@component('components.themes.default.radio',[
    'label' => '$LABEL$',
    'name' => '$NAME$',
    'value' => '$VALUE$'
    'options' => [['label' => '$OPTIONLABEL$', 'value' => '$OPTIONVALUE$']],
    'helpText' => '$HELPTEXT$',
])@endcomponent
```
---

Select
---
```php
@component('components.themes.default.select',[
    'label' => '$LABEL$',
    'name' => '$NAME$',
    'value' => old('$NAME$', $MODEL$->$NAME$),
    'helpText' => '$HELPTEXT$',
    'options' => $$$NAME$Options,
    'optionValueKey' => '$optionValueKey$',
    'optionTextKey'  => '$optionTextKey$',
    'leftCol'        => '$leftCol$',
    'rightCol'       => '$rightCol$',
])@endcomponent
```
---

File
---
```php
@component('components.themes.default.file',[
    'label' => '$label$',
    'name' => '$name$',
    'value' => $value$,
    'isImage' => $isImage$,
    'helpText' => '$helptext$',
    'prepend' => '$prepend$',
    'append' => '$append$',
])@endcomponent
```

Label
---
```php
@component('components.themes.default.label',[
    'name' => '$name$',
    'label' => '$label$',
    'value' => $model$->$name$,
    'types' => [ $types$ ],
    'exclude' => [ $exclude$ ]
])@endcomponent

```
---

Map
---
```php
@component('components.themes.default.map',[
    'label' => '$label$',
    'name' => '$name$',
    'value' => $$$model$->$name$,
    'helpText' => '$helpText$',
    'placeholder' => '$placeholder$',
])@endcomponent
```
---

Double Input
---
```php
@component('components.themes.default.input-input',[
    'label'           => '$label$',
    'helpText'        => '$helpText$',
    
    'name1'           => '$name1$',
    'value1'           => $$$value1$->$name1$,
    'prepend1'         => '$prepend1$',
    'append1'          => '$append1$',
    'options1'         =>  $options1$,
    'option1ValueKey' => '$option1ValueKey$',
    'option1TextKey'  => '$option1TextKey$',

    'name2'           => '$name2$',
    'value2'           => $$$value2$->$name2$,
    'prepend2'         => '$prepend2$',
    'append2'          => '$append2$',
    'options2'        =>  $options2$,
    'option2ValueKey' => '$option2ValueKey$',
    'option2TextKey'  => '$option2TextKey$',
])@endcomponent
```
---

Double Select
---
```php
@component('components.themes.default.select-select',[
    'label'           => '$label$',
    'helpText'        => '$helpText$',
    
    'name1'           => '$name1$',
    'value1'           => $$$value1$->$name1$,
    'prepend1'         => '$prepend1$',
    'append1'          => '$append1$',
    'options1'         =>  $options1$,
    'option1ValueKey' => '$option1ValueKey$',
    'option1TextKey'  => '$option1TextKey$',

    'name2'           => '$name2$',
    'value2'           => $$$value2$->$name2$,
    'prepend2'         => '$prepend2$',
    'append2'          => '$append2$',
    'options2'        =>  $options2$,
    'option2ValueKey' => '$option2ValueKey$',
    'option2TextKey'  => '$option2TextKey$',
])@endcomponent
```
---

Input and Select
---
```php
@component('components.themes.default.input-select',[
    'type' => '$TEXT$',
    'label' => '$LABEL$',
    'name' => '$NAME$',
    'value' => $VALUE$->$NAME$,
    'selectName' => '$selectName$',
    'selectValue' => $VALUE$->$selectName$,
    'prepend' => '$prepend$',
    'append' => '$append$',
    'options' => $options$,
    'optionValueKey' => '$optionValueKey$',
    'optionTextKey' => '$optionTextKey$',
    'selectPrepend' => '$selectPrepend$',
    'selectAppend' => '$selectAppend$',
    'helpText' => '$HELPTEXT$',
    'placeholder' => '$PLACEHOLDER$',
])@endcomponent
```
---

Head Toolbar
---
```php
'toolbar' => [
    [
        'label' => '$LABEL$',
        'url' => $URL$
    ]
]
```
---

Nav Item
---
```php
<li class="nav-item">
    <a class="nav-link{{active('$PATH$')}}" href="$URL$">$MENU$</a>
</li>
```
---

Nav Item Array
---
```php
[
    'label' => '$LABEL$',
    'url' => '$URL$',
    'path' => '$PATH$'
],
```
---

Nav Item Submenu
---
```php
<li class="nav-item">
    <a class="nav-link{{active('$PATH$')}}" href="$URL$"
       data-toggle="collapse" data-target="#$SUBID$$"
       aria-controls="$SUBID$$"
       aria-expanded="false">$MENU$</a>
    <ul class="flex-column collapse hide" id="$SUBID$$">
        <li class="nav-item">
            <a class="nav-link" href="$URL$/$SUBURL$">$SUBMENU$</a>
        </li>
    </ul>
</li>
```
---

Nav Tab Base
---
```php
<ul class="nav nav-tabs " id="$id$" role="tablist">
    $TABITEM$
</ul>
```
---

Nav Tab Item
---
```php
@component('components.nav-tab-item', [
    'label' => '$label$',
    'id' => '$id$',
    'url' => $url$,
    'tab' => $tab$
])@endcomponent
```
---

Sidebar
---
```php
@component('components.sidebar.sidebar-base',['id' => '$ID$'])
    $COMPONENT$
@endcomponent
```
---

Sidebar Parent Menu
---
```php
@component('components.sidebar.nav-parent',[
    'parentLabel' => '$ParentLabel$',
    'parentUrl' => '$ParentUrl$',
    'parentPath' => '$ParentPath$*',
    'subMenuId' => '$MenuId$SubMenu',
    'hideParent' => $hideParent$,
    'isChild' => $isChild$,
    'navItems' => [
        [
          'label' => '$SubMenuLabel$',
          'url' => '$SubMenuUrl$',
          'path' => '$SubMenuPath$'
        ],
      ]
    ])
@endcomponent
```
---

Page Navigator
---
```php
@component('components.record-navigator', [
    'heading' => '$HEADING$',
    'route' => '$ROUTE$',
    'previous' => $PREV$,
    'next' => $NEXT$
])@endcomponent

$END$
```
---

Record Navigator
---
```php
@component('components.record-navigator', [
    'heading'=> $HEADING$,
    'route' => '$ROUTE$',
    'previous' => $previous,
    'next' => $next
])@endcomponent
```
---
