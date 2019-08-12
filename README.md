
![Clone Form Preview](http://demo.examruler.com/clone-html-from/example.png)


Demo
-----

* [Demo 1](http://demo.examruler.com/clone-html-from//) - (Address Book).




```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/select2/3.3.2/select2.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/select2/3.3.2/select2.css">
<script src="cloneData.js" type="text/javascript"></script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">


<div class="container">
    <div class="margin-t-md">

        <div class="customer-form">
        <h3>Dynamic Form</h3>
            <form id="" action="/create" method="post" role="form">
                <div class="row">
                    <div class="col-sm-6">
                        <div class="form-group">
                            <label class="control-label" for="customer-first_name">First name</label>
                            <input type="text" id="customer-first_name" class="form-control" name="Customer[first_name]"
                                   maxlength="32" aria-required="true">

                            <p class="help-block help-block-error"></p>
                        </div>
                    </div>
                    <div class="col-sm-6">
                        <div class="form-group field-customer-last_name required">
                            <label class="control-label" for="customer-last_name">Last name</label>
                            <input type="text" id="customer-last_name" class="form-control" name="Customer[last_name]"
                                   maxlength="64" aria-required="true">

                        </div>
                    </div>
                </div>

                <div class="row">
                    <div class="col-sm-6">
                        <div class="form-group">
                            <label class="control-label" for="customer-email">Email</label>
                            <input type="text" id="customer-email" class="form-control" name="Customer[email]"
                                   maxlength="32" aria-required="true">

                            <p class="help-block help-block-error"></p>
                        </div>
                    </div>
                    <div class="col-sm-6">
                        <div class="form-group field-customer-last_name required">
                            <label class="control-label" for="customer-mobile">Mobile</label>
                            <input type="text" id="customer-mobile" class="form-control" name="Customer[mobile]"
                                   maxlength="64" aria-required="true">

                        </div>
                    </div>
                </div>

                <div id="main-container">
                    <div class="panel panel-default">

                        <div class="panel-body container-item">
                            <fieldset class="item panel panel-default" style="border: 1px solid black; padding: 10px;">
                                <!-- widgetBody -->
                                <legend style="width: auto;padding:10px;">Address: 1</legend>
                                <div class="panel-body">
                                    <div class="form-group">
                                        <label class="control-label" for="full_name_0">Full name</label>
                                        <input type="text" id="full_name_0" class="form-control"
                                               name="Address[0][full_name]" maxlength="128">
                                    </div>
                                    <div class="row">
                                        <div class="col-sm-6">
                                            <div class="form-group">
                                                <label class="control-label" for="address_line_one_0">Address line
                                                    1</label>
                                                <input type="text" id="address_line_one_0" class="form-control"
                                                       name="Address[0][address_line1]" maxlength="255">
                                                <p class="help-block help-block-error"></p>
                                            </div>
                                        </div>
                                        <div class="col-sm-6">
                                            <div class="form-group">
                                                <label class="control-label" for="address_line_two_0">Address line
                                                    2</label>
                                                <input type="text" id="address_line_two_0" class="form-control"
                                                       name="Address[0][address_line2]" maxlength="255">
                                                <p class="help-block help-block-error"></p>
                                            </div>
                                        </div>
                                    </div>

                                    <div class="row">
                                        <div class="col-sm-6">
                                            <div class="form-group">
                                                <label class="control-label" for="city_0">City</label>
                                                <input type="text" id="city_0" class="form-control"
                                                       name="Address[0][city]" maxlength="64">
                                                <p class="help-block help-block-error"></p>
                                            </div>
                                        </div>


                                        <div class="col-sm-6">
                                            <div class="form-group">
                                                <label class="control-label" for="state_0">State</label>

                                                <select id="state_0" class="form-control select2"
                                                        name="Address[0][city]">
                                                    <option value="" data-select2-id="2">Select a state ...</option>
                                                    <optgroup label="Alaskan/Hawaiian Time Zone">
                                                        <option value="AK">Alaska</option>
                                                        <option value="HI">Hawaii</option>
                                                    </optgroup>
                                                    <optgroup label="Pacific Time Zone">
                                                        <option value="CA">California</option>
                                                        <option value="NV">Nevada</option>
                                                        <option value="OR">Oregon</option>
                                                        <option value="WA">Washington</option>
                                                    </optgroup>
                                                </select>
                                            </div>
                                        </div>

                                    </div>
                                    <div>
                                        <a href="javascript:void(0)"
                                           class="remove-item btn btn-sm btn-danger remove-social-media">Remove</a>
                                    </div>
                            </fieldset>
                        </div>

                    </div>
                </div>
                <hr>
                <div class="row">
                    <div class="col-sm-6">
                        <a class="pull-right btn btn-success btn-xs" id="add-more"><i
                                class="fa fa-plus"></i>
                            Add address</a>
                        <div class="clearfix"></div>
                    </div>

                    <div class="col-sm-6">
                        <div class="form-group">
                            <button type="submit" class="btn btn-primary">Submit</button>
                        </div>
                    </div>
                </div>


            </form>
        </div>
    </div>
</div>


<script>
    $('a#add-more').cloneData({
        mainContainerId: 'main-container', // Main container Should be ID
        cloneContainer: 'container-item', // Which you want to clone
        removeButtonClass: 'remove-item', // Remove button for remove cloned HTML
        removeConfirm: true, // default true confirm before delete clone item
        removeConfirmMessage: 'Are you sure want to delete?', // confirm delete message
        //append: '<a href="javascript:void(0)" class="remove-item btn btn-sm btn-danger remove-social-media">Remove</a>', // Set extra HTML append to clone HTML
        minLimit: 2, // Default 1 set minimum clone HTML required
        maxLimit: 5, // Default unlimited or set maximum limit of clone HTML
        defaultRender: 1, // Number of clone items rendered by default 
        init: function () {
            console.info(':: Initialize Plugin ::');
        },
        beforeRender: function () {
            console.info(':: Before rendered callback called');
        },
        afterRender: function () {
            console.info(':: After rendered callback called');
        },
        afterRemove: function () {
            console.warn(':: After remove callback called');
        },
        beforeRemove: function () {
            console.warn(':: Before remove callback called');
        }
    });

    $('.select2').select2({
        placeholder: 'Select a month'
    });
</script>
```
