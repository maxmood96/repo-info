<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.15`](#kibana81915)
-	[`kibana:9.3.4`](#kibana934)
-	[`kibana:9.4.0`](#kibana940)

## `kibana:8.19.15`

```console
$ docker pull kibana@sha256:659c9e7cf3ce70ab53ac8274fa57b8199d2bd336867229bb674e5e634dc96a7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.15` - linux; amd64

```console
$ docker pull kibana@sha256:f173ac2a7ee37fda526e27bf9a5ae12324007bd69c0dbe041a6ada2b78879713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449915785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b25fbe99baeee53d8de19ef916c2eab84b7c05d70a264b2aace41b001970bdc`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Fri, 01 May 2026 00:10:03 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 01 May 2026 00:10:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:20:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 01 May 2026 00:20:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 01 May 2026 00:20:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 01 May 2026 00:20:09 GMT
RUN fc-cache -v # buildkit
# Fri, 01 May 2026 00:20:09 GMT
WORKDIR /usr/share/kibana
# Fri, 01 May 2026 00:20:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 01 May 2026 00:20:09 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:20:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 01 May 2026 00:20:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 01 May 2026 00:20:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 01 May 2026 00:20:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 01 May 2026 00:20:10 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 01 May 2026 00:20:10 GMT
LABEL org.label-schema.build-date=2026-04-28T12:23:50.593Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d48edd90b6f2528225b2ad8633873238cce0df3b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.15 org.opencontainers.image.created=2026-04-28T12:23:50.593Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d48edd90b6f2528225b2ad8633873238cce0df3b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.15
# Fri, 01 May 2026 00:20:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 01 May 2026 00:20:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 01 May 2026 00:20:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845151a6ca4dcac3d40e248edb0bfaef9102a6058247fa68db363a5d29ac33fd`  
		Last Modified: Fri, 01 May 2026 00:21:10 GMT  
		Size: 9.4 MB (9434349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb59fc12008c0ddd719b3aaaac4653f744aed7fd409e4c5290d3d725c49edf`  
		Last Modified: Fri, 01 May 2026 00:21:25 GMT  
		Size: 394.1 MB (394104455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd9f65314c7fe10f9bec87e64aadd3ccd3f35041bc58560394b520850c65a55`  
		Last Modified: Fri, 01 May 2026 00:21:10 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29220de0df96791617d56c996c9a8f8b2871f84aa114b15d01939fb84dc39a6`  
		Last Modified: Fri, 01 May 2026 00:21:11 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a6245c8c2e6196edff1b9239b6776afe407acbe780588d48170a80776d75bb`  
		Last Modified: Fri, 01 May 2026 00:21:11 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7710da17e199bd109ab1fa4060bae54f5c22992d8207bed16518bed0f26a8b0e`  
		Last Modified: Fri, 01 May 2026 00:21:12 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6462b41b8a6af10be84ea3cab5483680754038f7dd4993b8755aea80a0a7d80`  
		Last Modified: Fri, 01 May 2026 00:21:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bbb40319be3413586978256df476f695f52cb07caaf130bdcb32c73ff90df8`  
		Last Modified: Fri, 01 May 2026 00:21:13 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361c8f7ce56dbb51ee79e9a2cb18852e8fd7e627ddbffbe363506acf5f60922f`  
		Last Modified: Fri, 01 May 2026 00:21:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24aac25fca5211d4f1327821260358c9b9f9a1a522b959aaf92f5faaaeb70671`  
		Last Modified: Fri, 01 May 2026 00:21:14 GMT  
		Size: 161.7 KB (161741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6ffc1a588480584037be930ab3b0781ffef0675f48b029bb005ea65cbbc1bc`  
		Last Modified: Fri, 01 May 2026 00:21:14 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.15` - unknown; unknown

```console
$ docker pull kibana@sha256:6ef1e84a55c77f31f37f06c1a64754c8300b0f2a5a6df3e7ef90700ea7caded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5023620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b3a1ddd04751302d42cde41c68454c926a8c82a20f51bf53bd39ca652e61a2`

```dockerfile
```

-	Layers:
	-	`sha256:bf6f2e77874359264e09fdf105b3f882ed801fb03ce063b1fe48e392f599c943`  
		Last Modified: Fri, 01 May 2026 00:21:10 GMT  
		Size: 5.0 MB (4982705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20de668d886b002c6d3b4733588c39809c4edfffd6172452dc447b0eaf11cbcf`  
		Last Modified: Fri, 01 May 2026 00:21:10 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.15` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6079111dc2d44f076b023944440d289080ed7006b2d69e9740f7a8d35bf8b78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.3 MB (462308000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b713f77ee8e56f3218319f99d11900e16f3c46c32b2f488423643e5b2bdb01aa`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Fri, 01 May 2026 00:09:57 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 01 May 2026 00:09:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 May 2026 00:17:46 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 01 May 2026 00:17:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 01 May 2026 00:17:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 01 May 2026 00:17:47 GMT
RUN fc-cache -v # buildkit
# Fri, 01 May 2026 00:17:47 GMT
WORKDIR /usr/share/kibana
# Fri, 01 May 2026 00:17:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 01 May 2026 00:17:47 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 01 May 2026 00:17:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:17:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 01 May 2026 00:17:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 01 May 2026 00:17:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 01 May 2026 00:17:49 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 01 May 2026 00:17:49 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 01 May 2026 00:17:49 GMT
LABEL org.label-schema.build-date=2026-04-28T12:23:50.593Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d48edd90b6f2528225b2ad8633873238cce0df3b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.15 org.opencontainers.image.created=2026-04-28T12:23:50.593Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d48edd90b6f2528225b2ad8633873238cce0df3b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.15
# Fri, 01 May 2026 00:17:49 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 01 May 2026 00:17:49 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 01 May 2026 00:17:49 GMT
USER 1000
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36a57168d7bc687387ae7d814851fb11eda1897611f89e2899efd303092a2a6`  
		Last Modified: Fri, 01 May 2026 00:18:57 GMT  
		Size: 9.5 MB (9451970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc12ff13ffce9f0d34092fdc716156f31625f07348027fa42e21dfe291d1081c`  
		Last Modified: Fri, 01 May 2026 00:19:09 GMT  
		Size: 407.3 MB (407340145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc915a4bda4832ccceedd3d7a89dffa84fe8498503299f14775e002984868e0`  
		Last Modified: Fri, 01 May 2026 00:18:55 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4decbba5943dd917ab9517ba085294a1a3c5f79f8885dc51358dea4d3629dc0`  
		Last Modified: Fri, 01 May 2026 00:18:57 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc37740d42dc0d7320fd1cf85675f2e474c5aea1522a65b80f1f2db82b10da7`  
		Last Modified: Fri, 01 May 2026 00:18:57 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96935c7bc6684dc2929c3270afebe39ab51f1f0bc9c8f6d51388f99e16a55405`  
		Last Modified: Fri, 01 May 2026 00:18:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38087fd969b87f3cda2e964b59add6802bd66ae4f708073138746d50c4f2ce6d`  
		Last Modified: Fri, 01 May 2026 00:18:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34818d2cca51e7e00afc5738b7ded1202a8b7d56e5581b5dd60978b7f2a34ca4`  
		Last Modified: Fri, 01 May 2026 00:18:58 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ed52fd8d5941db48b3c24118af64360a964075f3a7d738bbbc38b12bdb17d9`  
		Last Modified: Fri, 01 May 2026 00:19:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1123bbcc6bfef065a8f54934094a4cf153d87023e64eee8be93d14265e79fcba`  
		Last Modified: Fri, 01 May 2026 00:19:00 GMT  
		Size: 158.3 KB (158261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d6f5940294a5449424ff6d418545d1da29e2d22937f37e307565d1d306059e`  
		Last Modified: Fri, 01 May 2026 00:19:00 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.15` - unknown; unknown

```console
$ docker pull kibana@sha256:e33b82fc336b432f9dcdb047f6662de8fc839438d1910fdd3ebeefa64fd18f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5024932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f3f8ec97d5e484b72f3ceaa69933846ad4717ee07e9200877a1570d050e625`

```dockerfile
```

-	Layers:
	-	`sha256:e0aaf97729be5452d62a2a56de94de662ae47fceac83899d0d278a273e0cba98`  
		Last Modified: Fri, 01 May 2026 00:18:56 GMT  
		Size: 5.0 MB (4983769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c39e3d095f5bf0d13a548b75abfb830558c9718c15436ddbfd0aecfc990ebbb`  
		Last Modified: Fri, 01 May 2026 00:18:56 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.4`

```console
$ docker pull kibana@sha256:c8ba09b19e8f77a95dfd53f86bf22514157896d065c248f64cefd82671382edf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.4` - linux; amd64

```console
$ docker pull kibana@sha256:3c3539f237e537e4780948670f8e0e3b6b84c575739f4eca9f331672a7233133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.7 MB (461701460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100b1746030ca29397a273ac315da6a4fc4ecf7782cdeebdddf3c1c5b26667fc`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:21:41 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 08 May 2026 16:21:41 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 08 May 2026 16:29:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 08 May 2026 16:29:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:29:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 08 May 2026 16:29:47 GMT
RUN fc-cache -v # buildkit
# Fri, 08 May 2026 16:29:47 GMT
WORKDIR /usr/share/kibana
# Fri, 08 May 2026 16:29:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 08 May 2026 16:29:47 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:29:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:29:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 08 May 2026 16:29:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:29:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 08 May 2026 16:29:49 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 08 May 2026 16:29:49 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 08 May 2026 16:29:49 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Fri, 08 May 2026 16:29:49 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 08 May 2026 16:29:49 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:29:49 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 08 May 2026 16:29:49 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 08 May 2026 16:29:49 GMT
USER 1000
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc95f9c476ca511e7915a5ca6b5caea62ecb12ed14bb1e5a3dc90306fac0054`  
		Last Modified: Fri, 08 May 2026 16:30:50 GMT  
		Size: 19.5 MB (19521480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513ee732a047d2529877f5747860295089b4de42f30d1529e58a32860640555b`  
		Last Modified: Fri, 08 May 2026 16:30:58 GMT  
		Size: 385.6 MB (385626802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad037e48309a0b804f4b14b6841b0ffa2c299099c98d6d8df8641f39ec173d6a`  
		Last Modified: Fri, 08 May 2026 16:30:49 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dd5b94eb16efd862db7bc7397c098c2b619b15db5d79088ebdc1332c657baa`  
		Last Modified: Fri, 08 May 2026 16:30:50 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c28502e0296c73aac27732229036a73f581cbd1fe077085fc96947fcecd5a4`  
		Last Modified: Fri, 08 May 2026 16:30:50 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ae8a9c57705ad56d12546a649d133ba1198d57d1000d87a02d53d7313042b`  
		Last Modified: Fri, 08 May 2026 16:30:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caf4bb178fba828fb947bfcd2fcad8db71e880b95149316fa022298731d9b30`  
		Last Modified: Fri, 08 May 2026 16:30:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc0274f523cc39e6f625b1eb9902e40f72596259c1e78d95087f7709e8fdf0`  
		Last Modified: Fri, 08 May 2026 16:30:52 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9306efc4d298b2650f7324043da3aecad3ed2eedd44dc3e78dfc62a4492b87fb`  
		Last Modified: Fri, 08 May 2026 16:30:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b309f32c2090a9642c468178baa435d08c8d95bc4a7f8b0cc4e343fa3770c67f`  
		Last Modified: Fri, 08 May 2026 16:30:53 GMT  
		Size: 74.5 KB (74542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46cfcf2627004415ca69347287c1adc6592453ce0af1283bd5de89992524b2b`  
		Last Modified: Fri, 08 May 2026 16:30:53 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde75c27332d4732eac642f29529331e314184ce834f15aaf6d902bd381bd08`  
		Last Modified: Fri, 08 May 2026 16:30:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:bb3e02be957c271822f7c223406133391f37905fbc1e017eed0b7b33794a1663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5865073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f759a974197f107323396371c6f5dee9058c74d8e8a3bd8d431371dee7025734`

```dockerfile
```

-	Layers:
	-	`sha256:080ecc4b2b1d9785a76e4d85164971cd0202a34beb3f399df722c92b95b98d9e`  
		Last Modified: Fri, 08 May 2026 16:30:49 GMT  
		Size: 5.8 MB (5821847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc56a3b1ff7e23caa97260c73d2e82e2a967e7bb2def04081ad9a512555f691`  
		Last Modified: Fri, 08 May 2026 16:30:49 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d152ded1297e3267fde68dc8c15c7af73bf1c0e5b38bbbea7cabd484380fc32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473066176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8373e0e5b575eeee1abecf17054cfeef8a74db7e0fdfe91a175e17146d2961`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:21:33 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 08 May 2026 16:21:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 08 May 2026 16:28:07 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 08 May 2026 16:28:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:28:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 08 May 2026 16:28:08 GMT
RUN fc-cache -v # buildkit
# Fri, 08 May 2026 16:28:08 GMT
WORKDIR /usr/share/kibana
# Fri, 08 May 2026 16:28:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 08 May 2026 16:28:08 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:28:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:28:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 08 May 2026 16:28:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:28:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 08 May 2026 16:28:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 08 May 2026 16:28:10 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 08 May 2026 16:28:10 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Fri, 08 May 2026 16:28:10 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 08 May 2026 16:28:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:28:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 08 May 2026 16:28:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 08 May 2026 16:28:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d1634331f6f551964af04d818e3a74b4fc358fce04d62728911a760755cb5`  
		Last Modified: Fri, 08 May 2026 16:29:17 GMT  
		Size: 19.5 MB (19466010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599569856af26fc4a8eadd8d6a09bc42e7123248f907b6fa8f01aa8025c5f99c`  
		Last Modified: Fri, 08 May 2026 16:29:25 GMT  
		Size: 398.8 MB (398837595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053c5b1a499b848b923dac5419e0490b900fb8a72ad911dbf3f425ba314484fc`  
		Last Modified: Fri, 08 May 2026 16:29:16 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953f309a2a55e1c9f14e09e87855bdbc06be676ba9ba3315b7a937af04ffb0fd`  
		Last Modified: Fri, 08 May 2026 16:29:17 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cbcdb5658df238a87e1b1845940df8c4711b514227a494034de7c1d7b6648b`  
		Last Modified: Fri, 08 May 2026 16:29:18 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239e0c6f1326c5bcfabf0c9b022dfe9de4fcc23b7362d81913323f39537493c`  
		Last Modified: Fri, 08 May 2026 16:29:19 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34586deb88aa080ac49da72754d97c27de71ff424fc1e4001a1979accdc650a8`  
		Last Modified: Fri, 08 May 2026 16:29:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ff1945a41d824bfecf05dc8d2322fb671fc7d0d6bb1b194c1db982f06033f`  
		Last Modified: Fri, 08 May 2026 16:29:20 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633eb81b2c4f67007e707f6abfb774e59e7418b034e71820df5bb4b26466e3c3`  
		Last Modified: Fri, 08 May 2026 16:29:21 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d77393e951d037c2199498ed1607bf59d8d02caf145db95ffd3f475f180f764`  
		Last Modified: Fri, 08 May 2026 16:29:21 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c081db490f55592161ce04f3cca0768eb10841fb8ad17363eb20621a065b7bfe`  
		Last Modified: Fri, 08 May 2026 16:29:21 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07be0a4524f56b1bce599ea92dbed9c2fb5dcae5d45077255ef9fa6403974d23`  
		Last Modified: Fri, 08 May 2026 16:29:23 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:ad0411d3786dba564187dfd7f073afb845ed8efe65813a45cc5b85ddd5188608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5864002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7f2691f80bfd374bf58d7de6fc1340226fe4aa06dc036dd0550e1e61bcc60c`

```dockerfile
```

-	Layers:
	-	`sha256:199cc8e2d86ca7eeb8b5c86f7c667779929b0d5d7c421f6830d666b579828ef0`  
		Last Modified: Fri, 08 May 2026 16:29:16 GMT  
		Size: 5.8 MB (5820519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5ee53156f4915692592a879ed213660737a16c8b2f55af744198799465d99c`  
		Last Modified: Fri, 08 May 2026 16:29:16 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.0`

```console
$ docker pull kibana@sha256:53c0db95c33553c27f667e41efa042a4ed3f7fffd1a04cd3d78d2c755e9323b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.0` - linux; amd64

```console
$ docker pull kibana@sha256:7368d3655f1d8651a8e5f837a6fd5f8420883a4e41516eea64aeb3ce37492424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528211027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280de76772d04935784255f65c3742e7fd0d11b6a2aeceb5185018ced08b8d4c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:21:45 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 08 May 2026 16:21:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 08 May 2026 16:30:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 08 May 2026 16:30:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:30:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 08 May 2026 16:30:51 GMT
RUN fc-cache -v # buildkit
# Fri, 08 May 2026 16:30:51 GMT
WORKDIR /usr/share/kibana
# Fri, 08 May 2026 16:30:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 08 May 2026 16:30:51 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:30:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:30:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 08 May 2026 16:30:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:30:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 08 May 2026 16:30:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 08 May 2026 16:30:53 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 08 May 2026 16:30:53 GMT
LABEL org.label-schema.build-date=2026-04-30T16:38:11.955Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b2e39752e03b56f48f51943214475ddba1f8e974 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T16:38:11.955Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b2e39752e03b56f48f51943214475ddba1f8e974 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Fri, 08 May 2026 16:30:53 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 08 May 2026 16:30:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:30:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 08 May 2026 16:30:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 08 May 2026 16:30:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce14c587ab3aa25994136e1fd3c00cf6ac83b90e127b0db756494407ee4df52`  
		Last Modified: Fri, 08 May 2026 16:32:05 GMT  
		Size: 19.5 MB (19521539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623dfe496ff2a170fe414aff3135bd26324086d96fb13e9a533eb85df528354`  
		Last Modified: Fri, 08 May 2026 16:32:17 GMT  
		Size: 452.1 MB (452136297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7caa2699e86b31d33f4b3a19606dd5500da9c0986b42eaeb9f015c60323379`  
		Last Modified: Fri, 08 May 2026 16:32:04 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33092acca94fdaf75e0ff99279f222159a86edf884b52e5fb80fbed10df031de`  
		Last Modified: Fri, 08 May 2026 16:32:05 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa028e897cae809f77243b0b0aeb8ce7c26c7b6ad7d75f7c32861cde4189a9dd`  
		Last Modified: Fri, 08 May 2026 16:32:05 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a689ef597aabb778a48b3d5aa311e37de1ae0e749a12d453325cefd4c40e8a82`  
		Last Modified: Fri, 08 May 2026 16:32:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb4307efadb41183b7bd152bc33b71ead919ab4cfdb2f55f07d849cc4ecace2`  
		Last Modified: Fri, 08 May 2026 16:32:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b300cb6e0b19bbcd414b3565e7f204a06f05266afde09993bf955a322e0ac8a1`  
		Last Modified: Fri, 08 May 2026 16:32:07 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4a1d0ac191789f7fc9285a6045ea95caec1e6ed4936d0fd38d65be9cc48f01`  
		Last Modified: Fri, 08 May 2026 16:32:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0efaf6a6c4c1d0a2cd838baeaa0b9a27adaec6e921eb1e260adf6dd01f09d8f`  
		Last Modified: Fri, 08 May 2026 16:32:08 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e266c0fc6707395e028e8e0e1fdc1d7218e9e71893fe3f792c465b45fde02d9`  
		Last Modified: Fri, 08 May 2026 16:32:08 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce26a490024cf1022334dd90ef08546e679033c170a604687537657da041a02`  
		Last Modified: Fri, 08 May 2026 16:32:09 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.0` - unknown; unknown

```console
$ docker pull kibana@sha256:34a9a990ea74e7423698183c85d2f690b50bdbd3015a550832731e2346270c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3b0181ba919c19c23cff1b4fdbceecd3b52f933ac651b016dd20ab0afc48fa`

```dockerfile
```

-	Layers:
	-	`sha256:08c45a1217ad24839b6cce53a5bd77585f46c00c414ecf5d12ec468ab4755cb6`  
		Last Modified: Fri, 08 May 2026 16:32:04 GMT  
		Size: 5.9 MB (5884418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff2e8233228a54d0c1a780bcb3b91d10c7fe934692a37a0035c2383e3def6a9`  
		Last Modified: Fri, 08 May 2026 16:32:04 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5892b9da1f2501b23129b2e41a36004ea38015109637adb965bab830d1ce6ca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539237276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0bed187192be4dfa2cceba3c7d51f592678965053328e002e763050e09508d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:21:31 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 08 May 2026 16:21:31 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 08 May 2026 16:28:59 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 08 May 2026 16:29:00 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 08 May 2026 16:29:00 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 08 May 2026 16:29:00 GMT
RUN fc-cache -v # buildkit
# Fri, 08 May 2026 16:29:00 GMT
WORKDIR /usr/share/kibana
# Fri, 08 May 2026 16:29:00 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 08 May 2026 16:29:00 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 08 May 2026 16:29:00 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:29:00 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 08 May 2026 16:29:00 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:29:01 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 08 May 2026 16:29:02 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 08 May 2026 16:29:02 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 08 May 2026 16:29:02 GMT
LABEL org.label-schema.build-date=2026-04-30T16:38:11.955Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b2e39752e03b56f48f51943214475ddba1f8e974 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T16:38:11.955Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b2e39752e03b56f48f51943214475ddba1f8e974 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Fri, 08 May 2026 16:29:02 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 08 May 2026 16:29:02 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 08 May 2026 16:29:02 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 08 May 2026 16:29:02 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 08 May 2026 16:29:02 GMT
USER 1000
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf562dbd4f573f917a606a906321bec1b06c6c376189c06d44b8c3595e176e91`  
		Last Modified: Fri, 08 May 2026 16:30:21 GMT  
		Size: 19.5 MB (19466215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc88c2ca8dd30ecc22b2c73a5b30319b28b7efaf293251cb1dcebb4ff27a349`  
		Last Modified: Fri, 08 May 2026 16:30:31 GMT  
		Size: 465.0 MB (465008493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347ad7f6b2ffc83b578f6c23ffc29685b6a144ebd85c9512979f78e5a0c4dbe2`  
		Last Modified: Fri, 08 May 2026 16:30:19 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2fb6057df25a9f513fd6897b889f058fad01f1ddc3481543d64306cc852aa9`  
		Last Modified: Fri, 08 May 2026 16:30:21 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551f0e86c5d3edcf8c339fb65419fd1e55b3710592e95c1a858f09e9d259397`  
		Last Modified: Fri, 08 May 2026 16:30:21 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9876e27c3a085a2d26aea2d477c36ea76cce9d66871d2e335092dda9f658ce07`  
		Last Modified: Fri, 08 May 2026 16:30:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227eb45a3595f3e4cf4e015bddfd2f40addccb03d360e56ed647d58006dd5280`  
		Last Modified: Fri, 08 May 2026 16:30:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1a54af4d7a55b388c43d1d984123dcb491feca646cd7b887335288205e3809`  
		Last Modified: Fri, 08 May 2026 16:30:23 GMT  
		Size: 4.9 KB (4920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed4c0081dd65b86187aebe5299cbc73cdb20c3cb76f598ede84b07f528ff92`  
		Last Modified: Fri, 08 May 2026 16:30:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075727370f6ecf22af3c7b4e26006e9e685d48fbdb919a34c5c5fe4d74417364`  
		Last Modified: Fri, 08 May 2026 16:30:24 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964367b0b389df4b213cf22e7733fa2e92f81eeb010023a07478585fd094d51`  
		Last Modified: Fri, 08 May 2026 16:30:24 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638e5c0044be1acc15ac5e7eff4ed8dfb52f64b3fdf8fdeda8a2815b1598d2f4`  
		Last Modified: Fri, 08 May 2026 16:30:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.0` - unknown; unknown

```console
$ docker pull kibana@sha256:2d4239321f901fb6f39c31720bb5ae0303606e361258f647860c1f2e7484fefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f428f3e335751c070515a6c58977385df96bcf99737c6c0c4e72b219f900160`

```dockerfile
```

-	Layers:
	-	`sha256:ab2b4b0c27a0831c166c211f416eed970f96c7266c41afaf489819275be16ac9`  
		Last Modified: Fri, 08 May 2026 16:30:20 GMT  
		Size: 5.9 MB (5883090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e795fad8aa1d9cfe51e975ccafc0c787c3eaaf8eccfb31cc2952a4173f0159d`  
		Last Modified: Fri, 08 May 2026 16:30:19 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
