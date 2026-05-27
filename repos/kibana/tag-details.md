<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.15`](#kibana81915)
-	[`kibana:9.3.4`](#kibana934)
-	[`kibana:9.4.1`](#kibana941)

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
$ docker pull kibana@sha256:069bb72de07dc3b41fd1dc90cfeab8fa5f8202f1fad02e439e56cde0f839512a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.4` - linux; amd64

```console
$ docker pull kibana@sha256:198cd54ef97d89e6e1fbfdf198516868660bd589aae5e7d9b8c617517a7e99c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.2 MB (462204478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53999c42d094d4c3df4a6363d0a3f232382fa6a84626f95c7dea046fe1816588`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:11:15 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 May 2026 23:11:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 26 May 2026 23:20:18 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 May 2026 23:20:18 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 May 2026 23:20:18 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 May 2026 23:20:19 GMT
RUN fc-cache -v # buildkit
# Tue, 26 May 2026 23:20:19 GMT
WORKDIR /usr/share/kibana
# Tue, 26 May 2026 23:20:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 May 2026 23:20:19 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:20:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:20:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 May 2026 23:20:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:20:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 May 2026 23:20:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 May 2026 23:20:21 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 May 2026 23:20:21 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 26 May 2026 23:20:21 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 26 May 2026 23:20:21 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 26 May 2026 23:20:21 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 May 2026 23:20:21 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 May 2026 23:20:21 GMT
USER 1000
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6756780c2d0a0e5a80a73a075d5d6e9cb46651ef7fdbb79161de763143d8b4d6`  
		Last Modified: Tue, 26 May 2026 23:21:24 GMT  
		Size: 19.3 MB (19332205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796cff1fd9d5fb9ad6a98a3089b019c2b9076b7d429d54fde6de32f6e3fa8cf8`  
		Last Modified: Tue, 26 May 2026 23:21:31 GMT  
		Size: 385.6 MB (385605142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ef0ace5cfcd03c44ba6b4d510e72a9db65136d689e30ee3284bc3da4ccc506`  
		Last Modified: Tue, 26 May 2026 23:21:22 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546513d5bd923fc7fb9f3a19ea12f1287d0075badf4213d8a062bcfc0b94211c`  
		Last Modified: Tue, 26 May 2026 23:21:24 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd7364140177a94a58dcba0ab5820f9679695f11ece59425e14b38c10b7cffb`  
		Last Modified: Tue, 26 May 2026 23:21:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce3b5e3f3a2c5b20e29bb2dd3c550b430050df68b36cf4438e0b1c6e3a28a62`  
		Last Modified: Tue, 26 May 2026 23:21:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a722112ec87a675c507c9ea2ab84bcefd0802e95e8ee445470a81d7fa004a5`  
		Last Modified: Tue, 26 May 2026 23:21:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8709dd726e40a6fa8fbec98ab77cb16b572ade7b6afbdc8b66629a274f9493c3`  
		Last Modified: Tue, 26 May 2026 23:21:26 GMT  
		Size: 4.9 KB (4915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2daa3aba700ddbbadeec5da2cd9d512ee6f442a80dc62fc41bf4b4d78d09993`  
		Last Modified: Tue, 26 May 2026 23:21:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f317338a9c5757b18eb49a04c9f7ec582f9da3bd5e1eeb52a0328c04f3aa3ab`  
		Last Modified: Tue, 26 May 2026 23:21:27 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887fc1a311713df5a524cd745c70234d3c98f72bc9f8ff1c325b24dcde2f2c5c`  
		Last Modified: Tue, 26 May 2026 23:21:27 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf54835b213aad2400de3524c0ffe52c7f0ac02633355d9fdaef7c0cbda281c`  
		Last Modified: Tue, 26 May 2026 23:21:28 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:8e0a9ef91c29cb86fdd9316efc59005220bd50dbf05209fb02915b659a68259e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5865491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3329f57b9cb8472b4abed6a0351849bfad87720b1e6c6e2713d3e234b4a8c5ed`

```dockerfile
```

-	Layers:
	-	`sha256:ead334253a188b4042194e37f426b4b19ac5df9bc0efcc6f5f36a4d262d7a9a7`  
		Last Modified: Tue, 26 May 2026 23:21:23 GMT  
		Size: 5.8 MB (5822265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f3ed77aa2486fcbca0241326db6ff54267cd0953faf64b8d3a1b48620fd5af`  
		Last Modified: Tue, 26 May 2026 23:21:22 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:95e33722ab772479f1908b63a60602dd4dd7fdd7465e25ac99f4362c493f2611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.5 MB (473520439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3f24cb9b67daf48e65056e041a1b64315212a48857b65666bce9e853948676`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:10:45 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 May 2026 23:10:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 26 May 2026 23:17:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 May 2026 23:17:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 May 2026 23:17:15 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 May 2026 23:17:15 GMT
RUN fc-cache -v # buildkit
# Tue, 26 May 2026 23:17:15 GMT
WORKDIR /usr/share/kibana
# Tue, 26 May 2026 23:17:15 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 May 2026 23:17:15 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:17:15 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:17:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 May 2026 23:17:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:17:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 May 2026 23:17:17 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 May 2026 23:17:17 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 May 2026 23:17:17 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 26 May 2026 23:17:17 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 26 May 2026 23:17:17 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 26 May 2026 23:17:17 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 May 2026 23:17:17 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 May 2026 23:17:17 GMT
USER 1000
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f660dd2235ccb975e0e4ba2a033f4985d73f9299d2a9498ed0bb24d407621d`  
		Last Modified: Tue, 26 May 2026 23:18:22 GMT  
		Size: 19.3 MB (19293976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114546a1b4ea17db12e3918b60114bf8b4e4774112546004bfc1abbaed2d10bf`  
		Last Modified: Tue, 26 May 2026 23:18:29 GMT  
		Size: 398.8 MB (398829413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7d6848d2bcf092f404475a02c02cda4b9e253135ad8792ba9e27a42c3967f`  
		Last Modified: Tue, 26 May 2026 23:18:20 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9f348a40da46a3ae9e57fe221cdf23b00c782d5d78903f48347c27bf29c72b`  
		Last Modified: Tue, 26 May 2026 23:18:22 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5aefce65bd2ba5191f082c2c1a474f2826373f643d414f416b22e2e83937fc`  
		Last Modified: Tue, 26 May 2026 23:18:22 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6315a5c94254c90400b9fab7503997bba68c9786cb9ebc1db87e3f6e68232f`  
		Last Modified: Tue, 26 May 2026 23:18:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e5773fbeb2690a9c022020d58700f6dfa5aba474133305bf6e75f57e12887c`  
		Last Modified: Tue, 26 May 2026 23:18:23 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe86087c5f90bc5eb1c51dbdbc9fc8a99308b7ed0ed7862c9020a68ef64801d`  
		Last Modified: Tue, 26 May 2026 23:18:24 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaae07460acc470cb05f0d30f7b47ea131633cc915fb89ec560abe18b2bc94d`  
		Last Modified: Tue, 26 May 2026 23:18:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05421173fb046f80d6d0e3bb6a6757587cf7d75430b17bfe3c30fc8bb98b9201`  
		Last Modified: Tue, 26 May 2026 23:18:25 GMT  
		Size: 73.5 KB (73454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12358229bc1520aa3d579b7d2596f37c08f56ada0f427973020e2bb7449989bc`  
		Last Modified: Tue, 26 May 2026 23:18:25 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a420be87f9fafbc9ce8101c3433fa97a5e9129f77093c46de6f389ef6bd4af0a`  
		Last Modified: Tue, 26 May 2026 23:18:26 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:725ed0484aadc37fd0d2bfec95a1c0bcb649d64bf8440532f56d27911b7e67a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5864420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bfd3d4d235ab975c9ce0b5e62c11148bdc5572da24a920241ba75640a5cb34`

```dockerfile
```

-	Layers:
	-	`sha256:30de36398ef4577d5ec130b46a6922827122f06c2c795b71e3c7c4445cf76221`  
		Last Modified: Tue, 26 May 2026 23:18:21 GMT  
		Size: 5.8 MB (5820937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73de2ab09a0b8dafb93380c0fa4423208060af78d18aa1bb5d2566802743734e`  
		Last Modified: Tue, 26 May 2026 23:18:21 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.1`

```console
$ docker pull kibana@sha256:4b29d11adf1bffeea2e277de4b0f18e747db8809b84a7a8706ad3f36dbe3d6c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.1` - linux; amd64

```console
$ docker pull kibana@sha256:9697660e6131d25cd734cd81106c12c98d90cb4bb28e3cf695eba97c4b555be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.5 MB (530476227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2b71237c9cea67ae3ede15323b367236203a22ba95fbadc29f3a0402a1c78e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Tue, 26 May 2026 23:11:19 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 May 2026 23:11:19 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 26 May 2026 23:20:44 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 May 2026 23:20:45 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 May 2026 23:20:45 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 May 2026 23:20:45 GMT
RUN fc-cache -v # buildkit
# Tue, 26 May 2026 23:20:45 GMT
WORKDIR /usr/share/kibana
# Tue, 26 May 2026 23:20:45 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 May 2026 23:20:45 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:20:45 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:20:45 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 May 2026 23:20:45 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:20:46 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 May 2026 23:20:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 May 2026 23:20:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 May 2026 23:20:47 GMT
LABEL org.label-schema.build-date=2026-05-08T16:12:32.674Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T16:12:32.674Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1
# Tue, 26 May 2026 23:20:47 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 26 May 2026 23:20:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 26 May 2026 23:20:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 May 2026 23:20:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 May 2026 23:20:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cb8f808509dc482ac3c47eff05aca267c81d56a05f76dbf3c500ebfb3670ba`  
		Last Modified: Tue, 26 May 2026 23:21:57 GMT  
		Size: 19.3 MB (19332193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4951c676e5b0b618ea94c2bb0230895de805ddcc98f5c960314799d38d736f`  
		Last Modified: Tue, 26 May 2026 23:22:05 GMT  
		Size: 453.9 MB (453876915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25815c9133b1071728ff0f38560b05773801aff4bf59b2d1778909755ce7d403`  
		Last Modified: Tue, 26 May 2026 23:21:56 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe565a1c6fc3bef9d5defd74c280c359415b2afbcb18a2c618be1e8ab911fc`  
		Last Modified: Tue, 26 May 2026 23:21:57 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701df33c621543220ff567ad2bca2f2f827de39d0bfe2ec6922efd04f70eec8b`  
		Last Modified: Tue, 26 May 2026 23:21:57 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2613d1165c5fe50345419acd9f9e3fd6759e89368a16dc08ab883a4c2ed6bc1`  
		Last Modified: Tue, 26 May 2026 23:21:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dd62a48829dddf0f201b9c6a2bda14dcd56d71ec3a02fc874188ceb2899b5`  
		Last Modified: Tue, 26 May 2026 23:21:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de28aaa478bcc3292749a30baccbec34474e3e813b1238bd146a8cb623151618`  
		Last Modified: Tue, 26 May 2026 23:21:58 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb06738521685d64aeb91ecb513269e663b4e99b8d0be65bd78b2d133f5a2b6`  
		Last Modified: Tue, 26 May 2026 23:22:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597dbea3b4e6d1466f541856d7b809b420bf9d233a0f6695d735843f24283a2d`  
		Last Modified: Tue, 26 May 2026 23:22:00 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1c096154529bfe5c1360659c425104ffc98f5700961d6bbfbfaa7f2e167cf5`  
		Last Modified: Tue, 26 May 2026 23:22:00 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596bd501fd3cd265639cc2eb5b1aa4c4cad889d8f2a74325e87018b0a71de00b`  
		Last Modified: Tue, 26 May 2026 23:22:01 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.1` - unknown; unknown

```console
$ docker pull kibana@sha256:c3a1092d02141079e5e766eca7335b601afdf8cd1eb54bccbcd0e31dbcfd6f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4693bfed1ebe6caafaf6547c6023877ccd9267ce16a0904a6dcced402e3542f`

```dockerfile
```

-	Layers:
	-	`sha256:72afd8827c4414c709d43c6f582c4d93ee70af66595acb2dc8e2bf1417d91b95`  
		Last Modified: Tue, 26 May 2026 23:21:56 GMT  
		Size: 5.9 MB (5884702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e699b971d559e2d9aaced91dedca3e2acc10818090ff7811a280bc96a4ee4634`  
		Last Modified: Tue, 26 May 2026 23:21:56 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:c32eb448bfbcb71bb5eddca77dd0441324bcc488e2915f0841da4f0bca155c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.4 MB (541445506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac12ca80ee8a435080d4db40bebd2f1a8c2fcc0773306a9d728dcc081813de08`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Tue, 26 May 2026 23:10:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 May 2026 23:10:47 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 26 May 2026 23:17:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 May 2026 23:17:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 May 2026 23:17:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 May 2026 23:17:58 GMT
RUN fc-cache -v # buildkit
# Tue, 26 May 2026 23:17:58 GMT
WORKDIR /usr/share/kibana
# Tue, 26 May 2026 23:17:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 May 2026 23:17:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 May 2026 23:17:58 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:17:58 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 May 2026 23:17:58 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 May 2026 23:17:59 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 May 2026 23:18:00 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 May 2026 23:18:00 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 May 2026 23:18:00 GMT
LABEL org.label-schema.build-date=2026-05-08T16:12:32.674Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T16:12:32.674Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1
# Tue, 26 May 2026 23:18:00 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 26 May 2026 23:18:00 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 26 May 2026 23:18:00 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 May 2026 23:18:00 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 May 2026 23:18:00 GMT
USER 1000
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547d2dc1a577026b89d9f6617458e87bfe569a5b906ceccf59455341c6e1fb21`  
		Last Modified: Tue, 26 May 2026 23:19:19 GMT  
		Size: 19.3 MB (19293842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afb41d1f4966ba3adfdc3dbf5d017afe1c52bf60dec1d68836fb416a1947fd7`  
		Last Modified: Tue, 26 May 2026 23:19:28 GMT  
		Size: 466.8 MB (466754622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27713752e54fdc22a668b36331aad242ca4f66b6ebbf4164569e726bebd2923b`  
		Last Modified: Tue, 26 May 2026 23:19:17 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f30fa461216384d9aac04bcb29a8cf25846575a3308889027892ce557657d`  
		Last Modified: Tue, 26 May 2026 23:19:19 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd894056b90c645b2ccea6ae5e2de01b131bce28389cc080027aed9bdfa9344`  
		Last Modified: Tue, 26 May 2026 23:19:19 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8a2f86eb068a80019edcc91296b7ba2d09f1a8aaf3619d7278b849e229f6e9`  
		Last Modified: Tue, 26 May 2026 23:19:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c563681ff714b604ddb794404a91b57099b28fcb35464913b88858dafd571c27`  
		Last Modified: Tue, 26 May 2026 23:19:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34c0e1367c62c133bcf5dd02da0bdde275314d6fc1e8404422f85771f19342a`  
		Last Modified: Tue, 26 May 2026 23:19:21 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a9af8dbd608c3e9c4794f8e2fe9655c5cbcc06525ef968e69ff9f31b99d8b1`  
		Last Modified: Tue, 26 May 2026 23:19:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e874102e7d788bed9ae1e936adffe4380b35d9aafc42abdf0438ad3ed8971d`  
		Last Modified: Tue, 26 May 2026 23:19:22 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c83793a9ca6a6e75370f0767a04c37436b4d8e4dfe03e293865d63aa12862c4`  
		Last Modified: Tue, 26 May 2026 23:19:22 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c0bf7219444f57736c3a8107ccd5f043a693af51556fa6c76e567465f76a5`  
		Last Modified: Tue, 26 May 2026 23:19:23 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.1` - unknown; unknown

```console
$ docker pull kibana@sha256:92fc3e418eb536a5e4a884a06d38a874429c3da4510fd84aaf83da83c501cd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8901e6d8d2ca2d23984b7091d707499871967f3d380b4a48a266ad83c2854e9f`

```dockerfile
```

-	Layers:
	-	`sha256:9cee0958b916069c1a678b6eb1ff79422a7917b1097325138188e22476483a9b`  
		Last Modified: Tue, 26 May 2026 23:19:18 GMT  
		Size: 5.9 MB (5883374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49854a0af773846d9f41c5cc0514d11bdb0c63a8f96ebfcb074f9b59f091ea4`  
		Last Modified: Tue, 26 May 2026 23:19:18 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
