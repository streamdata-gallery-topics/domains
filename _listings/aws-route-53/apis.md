---
name: AWS Route 53
x-slug: aws-route-53
description: Amazon Route 53 is a highly available and scalable cloud Domain Name
  System (DNS) web service. It is designed to give developers and businesses an extremely
  reliable and cost effective way to route end users to Internet applications by translating
  names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers
  use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well.Amazon
  Route 53 effectively connects user requests to infrastructure running in AWS &ndash;
  such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3
  buckets &ndash; and can also be used to route users to infrastructure outside of
  AWS. You can use Amazon Route 53 to configure DNS health checks to route traffic
  to healthy endpoints or to independently monitor the health of your application
  and its endpoints. Amazon Route 53 Traffic Flow makes it easy for you to manage
  traffic globally through a variety of routing types, including Latency Based Routing,
  Geo DNS, and Weighted Round Robin&mdash;all of which can be combined with DNS Failover
  in order to enable a variety of low-latency, fault-tolerant architectures. Using
  Amazon Route 53 Traffic Flow&rsquo;s simple visual editor, you can easily manage
  how your end-users are routed to your application&rsquo;s endpoints&mdash;whether
  in a single AWS region or distributed around the globe. Amazon Route 53 also offers
  Domain Name Registration &ndash; you can purchase and manage domain names such as
  example.com and Amazon Route 53 will automatically configure DNS settings for your
  domains.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Domains
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/apis.md
specificationVersion: "0.14"
apis:
- name: AWS Route 53 API - Create Hosted Zone
  x-api-slug: 20130401hostedzone-post
  description: Creates a new public hosted zone, used to specify how the Domain Name
    System (DNS)routes traffic on the Internet for a domain, such as example.com,
    and its subdomains. ImportantPublic hosted zones can't be converted to a private
    hosted zone or vice versa.Instead, create a new hosted zone with the same name
    and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
    resource. The request body must include a documentwith a CreateHostedZoneRequest
    element. The response returns theCreateHostedZoneResponse element containing metadata
    about the hostedzone.Fore more information about charges for hosted zones, see
    Amazon Route 53 Pricing.Note the following:You can't create a hosted zone for
    a top-level domain (TLD).Amazon Route 53 automatically creates a default SOA record
    and four NS records for the zone.For more information about SOA and NS records,
    see NS and SOA Records that Amazon Route 53 Creates for a Hosted Zone in the Amazon
    Route 53 Developer Guide.If your domain is registered with a registrar other than
    Amazon Route 53, you must update thename servers with your registrar to make Amazon
    Route 53 your DNS service. For more information, seeConfiguring Amazon Route 53
    as your DNSService in the Amazon Route 53 Developer's Guide.After creating a zone,
    its initial status is PENDING. This means that itis not yet available on all DNS
    servers. The status of the zone changes to INSYNCwhen the NS and SOA records are
    available on all Amazon Route 53 DNS servers. When trying to create a hosted zone
    using a reusable delegation set, specify anoptional DelegationSetId, and Amazon
    Route 53 would assign those 4 NS records for the zone, instead ofallotting a new
    one.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/20130401hostedzone-post-openapi.md
- name: AWS Route 53 API - List Hosted Zones By Name
  x-api-slug: 20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get
  description: 'Retrieves a list of your hosted zones in lexicographic order. Send
    a GETrequest to the /2013-04-01/hostedzonesbyname resource. The response includes
    aHostedZones child element for each hosted zone created by the current AWSaccount.             ListHostedZonesByName
    sorts hosted zones by name with the labels reversed.For example:                  com.example.www.               Note
    the trailing dot, which can change the sort order in some circumstances.If the
    domain name includes escape characters or Punycode,ListHostedZonesByName alphabetizes
    the domain name using the escaped orPunycoded value, which is the format that
    Amazon Route 53 saves in its database. For example, to createa hosted zone for
    example.com, specify ex\344mple.com for the domain name.ListHostedZonesByName
    alphabetizes it as:                  com.ex\344mple.               The labels
    are reversed and alphabetized using the escaped value. For more informationabout
    valid domain name formats, including internationalized domain names, see DNS Domain
    Name Format in theAmazon Route 53 Developer Guide.Amazon Route 53 returns up to
    100 items in each response. If you have a lot of hosted zones, usethe MaxItems
    parameter to list them in groups of up to 100. The response includesvalues that
    help navigate from one group of MaxItems hosted zones to thenext:The DNSName and
    HostedZoneId elements in the responsecontain the values, if any, specified for
    the dnsname andhostedzoneid parameters in the request that produced the currentresponse.The
    MaxItems element in the response contains the value, if any, thatyou specified
    for the maxitems parameter in the request that produced thecurrent response.If
    the value of IsTruncated in the response is true, there are morehosted zones associated
    with the current AWS account. If IsTruncated is false, this response includes
    the last hosted zonethat is associated with the current account. The NextDNSName
    element andNextHostedZoneId elements are omitted from the response.The NextDNSName
    and NextHostedZoneId elements in theresponse contain the domain name and the hosted
    zone ID of the next hosted zone that isassociated with the current AWS account.
    If you want to list more hosted zones, makeanother call to ListHostedZonesByName,
    and specify the value ofNextDNSName and NextHostedZoneId in the dnsnameand hostedzoneid
    parameters, respectively.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get-openapi.md
- name: AWS Route 53 API - Create Hosted Zone
  x-api-slug: 20130401hostedzone-post
  description: Creates a new public hosted zone, used to specify how the Domain Name
    System (DNS)routes traffic on the Internet for a domain, such as example.com,
    and its subdomains. ImportantPublic hosted zones can't be converted to a private
    hosted zone or vice versa.Instead, create a new hosted zone with the same name
    and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
    resource. The request body must include a documentwith a CreateHostedZoneRequest
    element. The response returns theCreateHostedZoneResponse element containing metadata
    about the hostedzone.Fore more information about charges for hosted zones, see
    Amazon Route 53 Pricing.Note the following:You can't create a hosted zone for
    a top-level domain (TLD).Amazon Route 53 automatically creates a default SOA record
    and four NS records for the zone.For more information about SOA and NS records,
    see NS and SOA Records that Amazon Route 53 Creates for a Hosted Zone in the Amazon
    Route 53 Developer Guide.If your domain is registered with a registrar other than
    Amazon Route 53, you must update thename servers with your registrar to make Amazon
    Route 53 your DNS service. For more information, seeConfiguring Amazon Route 53
    as your DNSService in the Amazon Route 53 Developer's Guide.After creating a zone,
    its initial status is PENDING. This means that itis not yet available on all DNS
    servers. The status of the zone changes to INSYNCwhen the NS and SOA records are
    available on all Amazon Route 53 DNS servers. When trying to create a hosted zone
    using a reusable delegation set, specify anoptional DelegationSetId, and Amazon
    Route 53 would assign those 4 NS records for the zone, instead ofallotting a new
    one.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/20130401hostedzone-post-openapi.md
- name: AWS Route 53 API - Create Hosted Zone
  x-api-slug: 20130401hostedzone-post
  description: Creates a new public hosted zone, used to specify how the Domain Name
    System (DNS)routes traffic on the Internet for a domain, such as example.com,
    and its subdomains. ImportantPublic hosted zones can't be converted to a private
    hosted zone or vice versa.Instead, create a new hosted zone with the same name
    and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
    resource. The request body must include a documentwith a CreateHostedZoneRequest
    element. The response returns theCreateHostedZoneResponse element containing metadata
    about the hostedzone.Fore more information about charges for hosted zones, see
    Amazon Route 53 Pricing.Note the following:You can't create a hosted zone for
    a top-level domain (TLD).Amazon Route 53 automatically creates a default SOA record
    and four NS records for the zone.For more information about SOA and NS records,
    see NS and SOA Records that Amazon Route 53 Creates for a Hosted Zone in the Amazon
    Route 53 Developer Guide.If your domain is registered with a registrar other than
    Amazon Route 53, you must update thename servers with your registrar to make Amazon
    Route 53 your DNS service. For more information, seeConfiguring Amazon Route 53
    as your DNSService in the Amazon Route 53 Developer's Guide.After creating a zone,
    its initial status is PENDING. This means that itis not yet available on all DNS
    servers. The status of the zone changes to INSYNCwhen the NS and SOA records are
    available on all Amazon Route 53 DNS servers. When trying to create a hosted zone
    using a reusable delegation set, specify anoptional DelegationSetId, and Amazon
    Route 53 would assign those 4 NS records for the zone, instead ofallotting a new
    one.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/20130401hostedzone-post-openapi.md
- name: AWS Route 53 API - List Hosted Zones By Name
  x-api-slug: 20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get
  description: 'Retrieves a list of your hosted zones in lexicographic order. Send
    a GETrequest to the /2013-04-01/hostedzonesbyname resource. The response includes
    aHostedZones child element for each hosted zone created by the current AWSaccount.             ListHostedZonesByName
    sorts hosted zones by name with the labels reversed.For example:                  com.example.www.               Note
    the trailing dot, which can change the sort order in some circumstances.If the
    domain name includes escape characters or Punycode,ListHostedZonesByName alphabetizes
    the domain name using the escaped orPunycoded value, which is the format that
    Amazon Route 53 saves in its database. For example, to createa hosted zone for
    example.com, specify ex\344mple.com for the domain name.ListHostedZonesByName
    alphabetizes it as:                  com.ex\344mple.               The labels
    are reversed and alphabetized using the escaped value. For more informationabout
    valid domain name formats, including internationalized domain names, see DNS Domain
    Name Format in theAmazon Route 53 Developer Guide.Amazon Route 53 returns up to
    100 items in each response. If you have a lot of hosted zones, usethe MaxItems
    parameter to list them in groups of up to 100. The response includesvalues that
    help navigate from one group of MaxItems hosted zones to thenext:The DNSName and
    HostedZoneId elements in the responsecontain the values, if any, specified for
    the dnsname andhostedzoneid parameters in the request that produced the currentresponse.The
    MaxItems element in the response contains the value, if any, thatyou specified
    for the maxitems parameter in the request that produced thecurrent response.If
    the value of IsTruncated in the response is true, there are morehosted zones associated
    with the current AWS account. If IsTruncated is false, this response includes
    the last hosted zonethat is associated with the current account. The NextDNSName
    element andNextHostedZoneId elements are omitted from the response.The NextDNSName
    and NextHostedZoneId elements in theresponse contain the domain name and the hosted
    zone ID of the next hosted zone that isassociated with the current AWS account.
    If you want to list more hosted zones, makeanother call to ListHostedZonesByName,
    and specify the value ofNextDNSName and NextHostedZoneId in the dnsnameand hostedzoneid
    parameters, respectively.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get-openapi.md
- name: AWS Route 53 API - List Hosted Zones By Name
  x-api-slug: 20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get
  description: 'Retrieves a list of your hosted zones in lexicographic order. Send
    a GETrequest to the /2013-04-01/hostedzonesbyname resource. The response includes
    aHostedZones child element for each hosted zone created by the current AWSaccount.             ListHostedZonesByName
    sorts hosted zones by name with the labels reversed.For example:                  com.example.www.               Note
    the trailing dot, which can change the sort order in some circumstances.If the
    domain name includes escape characters or Punycode,ListHostedZonesByName alphabetizes
    the domain name using the escaped orPunycoded value, which is the format that
    Amazon Route 53 saves in its database. For example, to createa hosted zone for
    example.com, specify ex\344mple.com for the domain name.ListHostedZonesByName
    alphabetizes it as:                  com.ex\344mple.               The labels
    are reversed and alphabetized using the escaped value. For more informationabout
    valid domain name formats, including internationalized domain names, see DNS Domain
    Name Format in theAmazon Route 53 Developer Guide.Amazon Route 53 returns up to
    100 items in each response. If you have a lot of hosted zones, usethe MaxItems
    parameter to list them in groups of up to 100. The response includesvalues that
    help navigate from one group of MaxItems hosted zones to thenext:The DNSName and
    HostedZoneId elements in the responsecontain the values, if any, specified for
    the dnsname andhostedzoneid parameters in the request that produced the currentresponse.The
    MaxItems element in the response contains the value, if any, thatyou specified
    for the maxitems parameter in the request that produced thecurrent response.If
    the value of IsTruncated in the response is true, there are morehosted zones associated
    with the current AWS account. If IsTruncated is false, this response includes
    the last hosted zonethat is associated with the current account. The NextDNSName
    element andNextHostedZoneId elements are omitted from the response.The NextDNSName
    and NextHostedZoneId elements in theresponse contain the domain name and the hosted
    zone ID of the next hosted zone that isassociated with the current AWS account.
    If you want to list more hosted zones, makeanother call to ListHostedZonesByName,
    and specify the value ofNextDNSName and NextHostedZoneId in the dnsnameand hostedzoneid
    parameters, respectively.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/domains/master/_listings/aws-route-53/20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.rekognition.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.route.53.stack.network
- type: x-documentation
  url: http://docs.aws.amazon.com/Route53/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/route53/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=87
- type: x-pricing
  url: https://aws.amazon.com/route53/pricing/
- type: x-registrar-policies
  url: https://aws.amazon.com/route53/amazon-registrar-policies/
- type: x-service-health
  url: http://status.aws.amazon.com/
- type: x-service-level-agreement
  url: https://aws.amazon.com/route53/sla
- type: x-sla
  url: https://aws.amazon.com/route53/sla/
- type: x-website
  url: https://aws.amazon.com/route53/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---