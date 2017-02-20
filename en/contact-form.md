---
lang: en
ref: contact-form
nav: false
title: Contact Us
---
<form id="reservation-form" data-async data-target="#reservation-modal-body" method="post" action="//formspree.io/booking@durobeach.com" class="form-horizontal">
  <div id="reservation-modal-body" class="modal-body">
    <fieldset>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_name">{{ site.data.i18n.['Name'][page.lang] }}</label>
        <div class="col-sm-9">
          <input id="id_name" name="name" type="text">
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_email">{{ site.data.i18n.['Email'][page.lang] }}</label>
        <div class="col-sm-9">
          <input id="id_email" name="email" type="email">
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_telephone">{{ site.data.i18n.['Telephone'][page.lang] }}</label>
        <div class="col-sm-9">
          <input id="id_telephone" name="telephone" type="text">
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_check_in">{{ site.data.i18n.['Check in'][page.lang] }}</label>
        <div class="col-sm-9">
          <input class="datepicker" data-date-format="dd/mm/yyyy" data-provide="datapicker-inline" id="id_check_in" name="check_in" type="text">
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_check_out">{{ site.data.i18n.['Check out'][page.lang] }}</label>
        <div class="col-sm-9">
          <input class="datepicker" data-date-format="dd/mm/yyyy" data-provide="datapicker-inline" id="id_check_out" name="check_out" type="text">
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_occupancy">{{ site.data.i18n.['Occupancy'][page.lang] }}</label>
        <div class="col-sm-9">
          <select id="id_occupancy" name="occupancy">
            <option value="2" selected="selected">{{ site.data.i18n.['Double occupancy'][page.lang] }}</option>
            <option value="1">{{ site.data.i18n.['Single occupancy'][page.lang] }}</option>
          </select>
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_room_arrangement">{{ site.data.i18n.['Room arrangement'][page.lang] }}</label>
        <div class="col-sm-9">
          <select id="id_room_arrangement" name="room_arrangement">
            <option value="2" selected="selected">{{ site.data.i18n.['Two single beds'][page.lang] }}</option>
            <option value="1">{{ site.data.i18n.['One King-Size bed'][page.lang] }}</option>
          </select>
        </div>
      </div>
      <div class="form-group">
        <label class="col-sm-3 control-label" for="id_comment">{{ site.data.i18n.['Comment'][page.lang] }}</label>
        <div class="col-sm-9">
          <textarea rows="10" cols="40" id="id_comment" name="comment"></textarea>
        </div>
      </div>
    </fieldset>
  </div>
  <div class="modal-footer">
    <a type="button" class="btn btn-danger btn-large" data-dismiss="modal">{{ site.data.i18n.['Cancel'][page.lang] }}</a>
    <input type="submit" class="btn btn-primary btn-large" value="{{ site.data.i18n['Submit'][page.lang] }}">
  </div>
  <input type="text" name="_gotcha" style="display:none" />
  <input type="hidden" name="_format" value="plain" />
  <input type="hidden" name="_subject" value="New reservation" />
</form>
