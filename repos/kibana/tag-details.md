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
$ docker pull kibana@sha256:ffed32747932446d4954ab8b7b4e3a27fefefdec4cb408ca851ea6d6981ced1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.4` - linux; amd64

```console
$ docker pull kibana@sha256:89c3009b5f2b29303be6e92ea0ad3156c8b05190ab57aa3f38c0639d21458ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.7 MB (461718856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e817c41d2d4bf6142765290d38d2bc8e9aab39db60d26f76c51cc70e90eb0de`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:09:23 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 05 May 2026 23:09:23 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 05 May 2026 23:18:49 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 05 May 2026 23:18:49 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:18:50 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 05 May 2026 23:18:50 GMT
RUN fc-cache -v # buildkit
# Tue, 05 May 2026 23:18:50 GMT
WORKDIR /usr/share/kibana
# Tue, 05 May 2026 23:18:50 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 05 May 2026 23:18:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:18:50 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:18:50 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 05 May 2026 23:18:50 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:18:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 05 May 2026 23:18:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 05 May 2026 23:18:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 05 May 2026 23:18:51 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 05 May 2026 23:18:51 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 05 May 2026 23:18:51 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:18:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 05 May 2026 23:18:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 05 May 2026 23:18:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072ed2377e1d013bb56bc1bdc970b8ee3ef88dec4e75e82012e2ef2aa5ebd183`  
		Last Modified: Tue, 05 May 2026 23:19:48 GMT  
		Size: 19.5 MB (19520027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd2ed125457b0706f8374ce8598b63bf561fe3b73f3f8d9a00e92c905b44409`  
		Last Modified: Tue, 05 May 2026 23:19:58 GMT  
		Size: 385.6 MB (385621318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db267a1ccbf4eb4361f8598a2d89ae26e365ab07614017ea8c6bcdb7892aa5f`  
		Last Modified: Tue, 05 May 2026 23:19:47 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895dbea8f5e4b19bf89681ee954bbcbf4ee56d40e4a90a4015d66bc78fb445c8`  
		Last Modified: Tue, 05 May 2026 23:19:48 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbca92a75d671c8811ae58b3f2044a087ab7e2938d7585dad67c34f688f88c29`  
		Last Modified: Tue, 05 May 2026 23:19:48 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c155e694e00c75c1f287e40316b67313491f6411b988820effed4fc0e957788`  
		Last Modified: Tue, 05 May 2026 23:19:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2450e672c42638ab232d20f277554f309faf607fff64125aa6d135d52a498ea`  
		Last Modified: Tue, 05 May 2026 23:19:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae023a17c9000ddcd5dfcca9f6cdb37923c7220d6e8b6885c253a694913db78`  
		Last Modified: Tue, 05 May 2026 23:19:50 GMT  
		Size: 4.9 KB (4914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d8f0d86e845e74d550eb56fee4554d87e6d212977dbb2d062c8909d08da5f2`  
		Last Modified: Tue, 05 May 2026 23:19:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ccf45a1e28a5e613aeb3c4dfa55160c0f1ab220b4a07b467cce8ee1e523b3e`  
		Last Modified: Tue, 05 May 2026 23:19:51 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563c808b21533e77768f153ffe0776f18317a75d029b6601f3f785039fb9edb7`  
		Last Modified: Tue, 05 May 2026 23:19:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a1df1c387dc1ee3308b35b524644771609c4a031d95854bd38763fdc9a354`  
		Last Modified: Tue, 05 May 2026 23:19:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:3caedec43f1a2b5a0533e0d091a6b4fadc4b10c47e7f2882dbd484439a7706f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5865073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7a5fdd2558bfd7710b8c60de146a9a7e4429fa9d94ba9dd2d1e36783ef50ff`

```dockerfile
```

-	Layers:
	-	`sha256:985fcd5caeaf217deb2eba96f404c33705f430ab71aa91f11dacb5aa144ffd9a`  
		Last Modified: Tue, 05 May 2026 23:19:48 GMT  
		Size: 5.8 MB (5821847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911f3997ec3247e6a875be6531085a2462ea755d142b42330330d48b2d60e4a5`  
		Last Modified: Tue, 05 May 2026 23:19:47 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:14bdd41b20f8d5c7da0d7fa9c8591fc1a12977a4302034a0c4d17a76f3a749c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473069577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed01266f1e975423680dde99b3de4391023145a1f8c9f95c1ef43e12acf7877`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:08:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 05 May 2026 23:08:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 05 May 2026 23:16:41 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 05 May 2026 23:16:41 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:16:41 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 05 May 2026 23:16:41 GMT
RUN fc-cache -v # buildkit
# Tue, 05 May 2026 23:16:41 GMT
WORKDIR /usr/share/kibana
# Tue, 05 May 2026 23:16:41 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 05 May 2026 23:16:41 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:16:41 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:16:42 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 05 May 2026 23:16:42 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:16:42 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 05 May 2026 23:16:43 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 05 May 2026 23:16:43 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 05 May 2026 23:16:43 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 05 May 2026 23:16:43 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 05 May 2026 23:16:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:16:44 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 05 May 2026 23:16:44 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 05 May 2026 23:16:44 GMT
USER 1000
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77cb4662c10e5e5adaaba8bd1b56e12f3a142a8e3142e755691b0373377d709`  
		Last Modified: Tue, 05 May 2026 23:17:50 GMT  
		Size: 19.5 MB (19468956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10ab29913f114001d12634f2b678b0a4c6a2f07218d46550c3150d8036d95b2`  
		Last Modified: Tue, 05 May 2026 23:17:56 GMT  
		Size: 398.8 MB (398837907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f474e808c7a94b881554ab1ed53c22f1829a6e57b365bba88fca98ba2c9a6e24`  
		Last Modified: Tue, 05 May 2026 23:17:48 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f528a5a90e8181b7232d2e8b0fe2d04d553fe1598b4ad24251d02f0cb65f8004`  
		Last Modified: Tue, 05 May 2026 23:17:49 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9b5b035a81e02ab13010d0f2668c9429ade8a1f3c4254cbe55dae6bf7dfbff`  
		Last Modified: Tue, 05 May 2026 23:17:49 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9f8cbbd91dcbfa03263dbeb13f529b2653ddd2dcf289bdce1b23244252d36e`  
		Last Modified: Tue, 05 May 2026 23:17:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a5c75ddd7d95bfbd4f5f543368bfd6982dad0032d0a05836fef6d1c31ce4f5`  
		Last Modified: Tue, 05 May 2026 23:17:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912dbd674479c34ab7e5f0c6760ec3dd35f6b17e127050f6550d1e135bc1c4bb`  
		Last Modified: Tue, 05 May 2026 23:17:51 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059f013d5a14462e274f60fdcf5c53781966433a96346c04eff8da0375364949`  
		Last Modified: Tue, 05 May 2026 23:17:52 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9b1094d3fe71e6c54b7d8b15e247d3e239808bf03ed875b7d89d2edc34438b`  
		Last Modified: Tue, 05 May 2026 23:17:52 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed4afe58ce159857ddfbb5f3bd128bdeb6e8f51cab2f52dea74f8f11a1a64f`  
		Last Modified: Tue, 05 May 2026 23:17:52 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc44605ca60a7cd970f012b55c273a76b1c754d87ee5f0a6f706e59e233b6ad`  
		Last Modified: Tue, 05 May 2026 23:17:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:fcaeca47ea20601033cb512145d0cc3236ade0154798e9fe1c56a9d16b294da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5864001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1123f6a98b4bf1ed00ca46d64951acbd72cc2882d2fed0d1dfcbe0c6f4db4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:6ce5d2a569bcd957b1dee0dd47bcc4551314097c69fc1a04baca88d31be69655`  
		Last Modified: Tue, 05 May 2026 23:17:49 GMT  
		Size: 5.8 MB (5820519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5def4d1ed395ffba03c1a4e6ada0b1fb88410f0c96eda9591a8a56a7dcf183`  
		Last Modified: Tue, 05 May 2026 23:17:48 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.0`

```console
$ docker pull kibana@sha256:de6f4172462778e2038ddada543407df1549ff57b21b529afdbfad41045dc616
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.0` - linux; amd64

```console
$ docker pull kibana@sha256:be192b1626f96cbe96a36696f00c117c9560e017ad88c4e3ba44ae5510f82a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528249034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f149863887083a741720cfa54b288749796bab65f8cd7b8f9b13fd542e0c696`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:09:22 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 05 May 2026 23:09:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 05 May 2026 23:19:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 05 May 2026 23:19:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:19:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 05 May 2026 23:19:56 GMT
RUN fc-cache -v # buildkit
# Tue, 05 May 2026 23:19:56 GMT
WORKDIR /usr/share/kibana
# Tue, 05 May 2026 23:19:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 05 May 2026 23:19:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:19:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:19:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 05 May 2026 23:19:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:19:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 05 May 2026 23:19:58 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 05 May 2026 23:19:59 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 05 May 2026 23:19:59 GMT
LABEL org.label-schema.build-date=2026-04-30T16:38:11.955Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b2e39752e03b56f48f51943214475ddba1f8e974 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T16:38:11.955Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b2e39752e03b56f48f51943214475ddba1f8e974 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Tue, 05 May 2026 23:19:59 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 05 May 2026 23:19:59 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:19:59 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 05 May 2026 23:19:59 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 05 May 2026 23:19:59 GMT
USER 1000
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fedb4300ba6d75cddd57bcfb225165777d5e42328949542bd1e962a1609e15`  
		Last Modified: Tue, 05 May 2026 23:21:11 GMT  
		Size: 19.5 MB (19520062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a69f41489686f75dc125b9363f8c0a180775b1b1fc7faf9159d2cb8808b0845`  
		Last Modified: Tue, 05 May 2026 23:21:20 GMT  
		Size: 452.2 MB (452151449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55d21b3bf8fb8626751b196cc2a9c13bdc322c657d3b76e1f95a8a2c0b008b`  
		Last Modified: Tue, 05 May 2026 23:21:09 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120dcee83066db9b2bc951aa7c7b604487fd5cbb15ed32b4032bd4dcd303abc6`  
		Last Modified: Tue, 05 May 2026 23:21:11 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c494ec74ad975e1cd62f651757af1366543f991c77950e2618752e0522756d8`  
		Last Modified: Tue, 05 May 2026 23:21:11 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b127a4d24317f3ca313187a56a6da7eb4a16da42b4ec9963356f9a09faae36`  
		Last Modified: Tue, 05 May 2026 23:21:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0e772101b5b848cdc4378367ea524864430fb20e1907af58c8be627a240dce`  
		Last Modified: Tue, 05 May 2026 23:21:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96593d11e8f933f23a0950b133611520f8dbb11770f7eb98574b828641c37c6`  
		Last Modified: Tue, 05 May 2026 23:21:13 GMT  
		Size: 4.9 KB (4915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773db0200b5e1df81233ff28ac17fee78eec5f6e30ddfb938633ca6c777012e2`  
		Last Modified: Tue, 05 May 2026 23:21:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f193801f68d585c27e124890e9102dad574f05e06afd73d584be6a9427d06220`  
		Last Modified: Tue, 05 May 2026 23:21:14 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f930c1b36d1aca081f849d4269a0869809a5ed7548f6a32f35652dab42e3163`  
		Last Modified: Tue, 05 May 2026 23:21:14 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b55241c6f5e766202c90b31254b4858de3264e6ffe8b9d42533d96a1d8381f`  
		Last Modified: Tue, 05 May 2026 23:21:15 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.0` - unknown; unknown

```console
$ docker pull kibana@sha256:05d2df64019f60a965705c3361e9ccf5beecba8a81aba9dffda2df58fe3e2e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5a2b574a02a61865d0a16969690a402147e69969f211af049b836525f0c402`

```dockerfile
```

-	Layers:
	-	`sha256:87089bb77db943c18f90998ff6500427e0e6b5c6801f940d9b32e976617f06fd`  
		Last Modified: Tue, 05 May 2026 23:21:11 GMT  
		Size: 5.9 MB (5884418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e983bbbdb9bf02bd9e820af4903232b64372288a12498d4f6850b8b120b544`  
		Last Modified: Tue, 05 May 2026 23:21:10 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:bd9620ca94bd2d9589a943470c3e1965e817ab396288d73f62e85fd07a655364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.3 MB (539251352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5a6ccc2f6eae5bc254df0fde85a02615dafdf31d016172af65a8a70cfea1a6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:09:04 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 05 May 2026 23:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 05 May 2026 23:17:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 05 May 2026 23:17:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 05 May 2026 23:17:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 05 May 2026 23:17:36 GMT
RUN fc-cache -v # buildkit
# Tue, 05 May 2026 23:17:36 GMT
WORKDIR /usr/share/kibana
# Tue, 05 May 2026 23:17:36 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 05 May 2026 23:17:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 05 May 2026 23:17:36 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:17:36 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 05 May 2026 23:17:36 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:17:37 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 05 May 2026 23:17:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 05 May 2026 23:17:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 05 May 2026 23:17:38 GMT
LABEL org.label-schema.build-date=2026-04-30T16:38:11.955Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b2e39752e03b56f48f51943214475ddba1f8e974 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T16:38:11.955Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b2e39752e03b56f48f51943214475ddba1f8e974 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Tue, 05 May 2026 23:17:38 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 05 May 2026 23:17:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 05 May 2026 23:17:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 05 May 2026 23:17:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 05 May 2026 23:17:38 GMT
USER 1000
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab7e141b69b3ab658a86b9ddf8be62257b17830385c23aabb80ab173cf24277`  
		Last Modified: Tue, 05 May 2026 23:18:57 GMT  
		Size: 19.5 MB (19468922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c044c94f76d517ca05966dc86e23214019ac0deb64090504ff3d52272795952f`  
		Last Modified: Tue, 05 May 2026 23:19:06 GMT  
		Size: 465.0 MB (465019713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af04909283ccae903ad30aa89c8763bfd63e99df785f01692acbf35ee4a572ea`  
		Last Modified: Tue, 05 May 2026 23:18:56 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be757d5351709a65436c3f3f49a2141e6a31842c616bc528bf572767b3ad2123`  
		Last Modified: Tue, 05 May 2026 23:18:57 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2537d14eae15bb0355533bfe57d2e11cb9ae4e2d702e33f442e421ac937f6cf`  
		Last Modified: Tue, 05 May 2026 23:18:57 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b5f423fa4af8b0c4a3971b961428d83102b5f395202f32dacf9b7a792cf233`  
		Last Modified: Tue, 05 May 2026 23:18:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0768411e4d245a67a4ab57ed8b98bbee79d71f1fe3e5e11a7d051b62062186de`  
		Last Modified: Tue, 05 May 2026 23:18:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358979a65ca2f65004e8b00840638719dc80fe181e234e31fd65ffa423d6a58c`  
		Last Modified: Tue, 05 May 2026 23:18:59 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1b6d7a3ea4dd8de96e45e650588a80ecc1dcfd925a7ee0428a2fbd639aeb4b`  
		Last Modified: Tue, 05 May 2026 23:19:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4499b133925355a6ed52846dc3b2f55c6b41bef5361eb2b20581501e9141c8b4`  
		Last Modified: Tue, 05 May 2026 23:19:00 GMT  
		Size: 73.5 KB (73452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56bb14e41549cc144c446d779d7e76e815303bc058a9035ff65ccd89d19cd5e`  
		Last Modified: Tue, 05 May 2026 23:19:00 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d940e3fa87fa87dbaae82d76a94a52be45ded143cbce32963670d6ef1477f397`  
		Last Modified: Tue, 05 May 2026 23:19:01 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.0` - unknown; unknown

```console
$ docker pull kibana@sha256:58bfac702cd76cfbc6e15a534dbae7ccebaa6a562c6fba574b9e796b5598a645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03961722af79c7182a23f1a550dabab49f32f2a7963bbf62efec6f5ef7308`

```dockerfile
```

-	Layers:
	-	`sha256:71947d0ad8e8ed24ba1662d804e2648493af72a705cdbfc169acd82a0a387857`  
		Last Modified: Tue, 05 May 2026 23:18:57 GMT  
		Size: 5.9 MB (5883090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1903c618cfef2fc8c86b5dc8adf6b5ef4995dc2c9e04901819ab39cb5839e16`  
		Last Modified: Tue, 05 May 2026 23:18:56 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
