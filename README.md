[![Build Status](https://app.travis-ci.com/cloudinary/cloudinary_gem.svg?branch=master)](https://app.travis-ci.com/github/cloudinary/cloudinary_gem)
[![Gem Version](https://badge.fury.io/rb/cloudinary.svg)](https://rubygems.org/gems/cloudinary)
[![Gem Version](https://badgen.net/rubygems/dt/cloudinary)](https://rubygems.org/gems/cloudinary)

# Why I am using this fork?

I have the same issue as this user: https://github.com/cloudinary/cloudinary_gem/issues/473 (2021)
and this one too: https://github.com/cloudinary/cloudinary_gem/pull/424 (2020)

But the cloundiary team as not addressed it for a long time now.

⚠️ Make sure this for is updated at a version you need ⚠️

## Changes
<img width="1104" alt="Screenshot 2022-02-24 at 12 18 35" src="https://user-images.githubusercontent.com/11267346/155505388-0530c4a5-c841-4c47-af47-12ce02f22b99.png">


call of this function in rails:
https://github.com/rails/rails/blob/1df9b01fe61dbd81f10dcf44cddd689270f6d8ba/activestorage/app/models/active_storage/blob.rb#L221
``` ruby
  # Returns a URL that can be used to directly upload a file for this blob on the service. This URL is intended to be
  # short-lived for security and only generated on-demand by the client-side JavaScript responsible for doing the uploading.
  def service_url_for_direct_upload(expires_in: ActiveStorage.service_urls_expire_in)
    service.url_for_direct_upload key, expires_in: expires_in, content_type: content_type, content_length: byte_size, checksum: checksum, custom_metadata: custom_metadata
  end
```















Cloudinary Ruby on Rails SDK
===================

## About

The Cloudinary Ruby on Rails SDK allows you to quickly and easily integrate your application with Cloudinary.
Effortlessly optimize, transform, upload and manage your cloud's assets.

#### Note

This Readme provides basic installation and usage information. For the complete documentation, see
the [Ruby on Rails SDK Guide](https://cloudinary.com/documentation/rails_integration).

## Table of Contents

- [Why I am using this fork?](#why-i-am-using-this-fork)
- [Cloudinary Ruby on Rails SDK](#cloudinary-ruby-on-rails-sdk)
  - [About](#about)
      - [Note](#note)
  - [Table of Contents](#table-of-contents)
  - [Key Features](#key-features)
  - [Version Support](#version-support)
  - [Installation](#installation)
- [Usage](#usage)
    - [Setup](#setup)
    - [Transform and Optimize Assets](#transform-and-optimize-assets)
    - [Upload](#upload)
    - [CarrierWave Integration](#carrierwave-integration)
    - [Active Storage Integration](#active-storage-integration)
    - [Security options](#security-options)
    - [Samples](#samples)
  - [Contributions](#contributions)
  - [Get Help](#get-help)
  - [About Cloudinary](#about-cloudinary)
  - [Additional Resources](#additional-resources)
  - [Licence](#licence)

## Key Features

- [Transform](https://cloudinary.com/documentation/rails_video_manipulation#video_transformation_examples) and
  [optimize](https://cloudinary.com/documentation/rails_image_manipulation#image_optimizations) assets.
- Generate [image](https://cloudinary.com/documentation/rails_image_manipulation#deliver_and_transform_images) and
  [video](https://cloudinary.com/documentation/rails_video_manipulation#rails_video_transformation_code_examples) tags.
- [Asset Management](https://cloudinary.com/documentation/rails_asset_administration).
- [Secure URLs](https://cloudinary.com/documentation/video_manipulation_and_delivery#generating_secure_https_urls_using_sdks)
  .

## Version Support

| SDK Version | Ruby 1.9.3 | Ruby 2.x | Ruby 3.x |
|-------------|------------|----------|----------|
| 1.x         | v          | v        | v        |

| SDK Version | Rails 5.x | Rails 6.x |
|-------------|-----------|-----------|
| 1.x         | v         | v         |

## Installation

```bash
gem install cloudinary
```

# Usage

### Setup

```ruby
require 'cloudinary'
```

### Transform and Optimize Assets
- [See full documentation](https://cloudinary.com/documentation/rails_image_manipulation).

```ruby
 cl_image_tag("sample.jpg", :width => 100, :height => 150, :crop => :fill)
```

### Upload
- [See full documentation](https://cloudinary.com/documentation/rails_image_and_video_upload).
- [Learn more about configuring your uploads with upload presets](https://cloudinary.com/documentation/upload_presets).

```ruby
Cloudinary::Uploader.upload("my_picture.jpg")
```

### CarrierWave Integration
- [See full documentation](https://cloudinary.com/documentation/rails_carrierwave).

### Active Storage Integration
- [See full documentation](https://cloudinary.com/documentation/rails_activestorage).

### Security options
- [See full documentation](https://cloudinary.com/documentation/solution_overview#security).

### Samples
 - See [samples folder](https://github.com/cloudinary/cloudinary_gem/tree/master/samples).

## Contributions
 - See [CONTRIBUTING](CONTRIBUTING.md).

## Get Help

If you run into an issue or have a question, you can either:

- Issues related to the SDK: [Open a GitHub issue](https://github.com/cloudinary/cloudinary_gem/issues).
- Issues related to your account: [Open a support ticket](https://cloudinary.com/contact)

## About Cloudinary

Cloudinary is a powerful media API for websites and mobile apps alike, Cloudinary enables developers to efficiently
manage, transform, optimize, and deliver images and videos through multiple CDNs. Ultimately, viewers enjoy responsive
and personalized visual-media experiences—irrespective of the viewing device.

## Additional Resources

- [Cloudinary Transformation and REST API References](https://cloudinary.com/documentation/cloudinary_references):
  Comprehensive references, including syntax and examples for all SDKs.
- [MediaJams.dev](https://mediajams.dev/): Bite-size use-case tutorials written by and for Cloudinary Developers
- [DevJams](https://www.youtube.com/playlist?list=PL8dVGjLA2oMr09amgERARsZyrOz_sPvqw): Cloudinary developer podcasts on
  YouTube.
- [Cloudinary Academy](https://training.cloudinary.com/): Free self-paced courses, instructor-led virtual courses, and
  on-site courses.
- [Code Explorers and Feature Demos](https://cloudinary.com/documentation/code_explorers_demos_index): A one-stop shop
  for all code explorers, Postman collections, and feature demos found in the docs.
- [Cloudinary Roadmap](https://cloudinary.com/roadmap): Your chance to follow, vote, or suggest what Cloudinary should
  develop next.
- [Cloudinary Facebook Community](https://www.facebook.com/groups/CloudinaryCommunity): Learn from and offer help to
  other Cloudinary developers.
- [Cloudinary Account Registration](https://cloudinary.com/users/register/free): Free Cloudinary account registration.
- [Cloudinary Website](https://cloudinary.com): Learn about Cloudinary's products, partners, customers, pricing, and
  more.

## Licence

Released under the MIT license.
