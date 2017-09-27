# User profiling

NearIT creates an anonymous profile for every user of your app. You can choose to add data to user profile. This data will be available inside recipes to allow the creation of user targets.

## Add user-data to NearIT

You can set user data with this method, it can be called multiple times to set several user data:
<div class="code-swift">
manager.setDeferredUserData("gender", value: "m")
</div>
<div class="code-objc">
[manager setDeferredUserDataWithKey:@"gender" value:@"m"];
</div>

Please remember: you will need to use the "**Settings> Data Mapping**" section of [NearIT](https://go.nearit.com) to configure the data fields to be used inside recipes.



## Save the profile ID!

If you can, we recommend you to store the NearIT profileID in your CRM database for two main reasons:

- it allows you to link our analytics to your users
- it allows to associate all the devices of an user to the same NearIT profile.


Getting the local profile ID of an user is easy:
<div class="code-swift">
manager.profileId
</div>
<div class="code-objc">
[manager profileId];
</div>


If you detect that your user already has a NearIT profileID in your CRM database (i.e. after a login), you should manually write it on a local app installation:
<div class="code-swift">
manager.setProfile(id: "your remote NearIT profile ID")
</div>
<div class="code-objc">
[manager setProfileId:@"your remote NearIT profile ID"];
</div>