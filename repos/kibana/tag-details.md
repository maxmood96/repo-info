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
$ docker pull kibana@sha256:29b49be3c75fca906a5512bc4f4a54a90cc84d4ea502715503ada0076b459f01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.4` - linux; amd64

```console
$ docker pull kibana@sha256:3f42ca9b272f748c88d73be014a89dc7d10a27dc0a24899debd5323518cf500a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.7 MB (461692554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e43da3ddeb01b4c446119c24caddd20ece4f4f5abdb1975c70568024942e584`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 11 May 2026 01:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:07:55 GMT
ENV container oci
# Mon, 11 May 2026 01:07:56 GMT
COPY dir:d396e6c334ec17a1ba4a03f21481f526666f77d114978313ef1df55edd8e1412 in /      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:07:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:07:39Z" "org.opencontainers.image.created"="2026-05-11T01:07:39Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:07:39Z
# Tue, 12 May 2026 00:06:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 May 2026 00:06:47 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 May 2026 00:13:31 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 May 2026 00:13:31 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 00:13:32 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 May 2026 00:13:32 GMT
RUN fc-cache -v # buildkit
# Tue, 12 May 2026 00:13:32 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2026 00:13:32 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 May 2026 00:13:32 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 00:13:32 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:13:32 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 May 2026 00:13:32 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 May 2026 00:13:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 May 2026 00:13:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 May 2026 00:13:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 May 2026 00:13:34 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 12 May 2026 00:13:34 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 May 2026 00:13:34 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 00:13:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 May 2026 00:13:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 May 2026 00:13:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec495137206b60664af4b39ddb8f1b52ec68b6e33686df98b7e0bdb1912f53d`  
		Last Modified: Tue, 12 May 2026 00:14:36 GMT  
		Size: 19.5 MB (19521790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d770afc1f42b351fb4e12e32b3bcdd03fc0c3164e26e1d336dbfe46653dbcb`  
		Last Modified: Tue, 12 May 2026 00:14:43 GMT  
		Size: 385.6 MB (385617629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281adf5ba90a6fc0d243f33c304e30d2b5b9169a4ad3fa64e196b99c70f2270a`  
		Last Modified: Tue, 12 May 2026 00:14:35 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de98300889691408c4fa8ea0ea9400810b3c4bff3b0ae56b67679115d6e1ec08`  
		Last Modified: Tue, 12 May 2026 00:14:36 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b3dc64e2ce9dfd7dadb7990a2a24288e9806d469514aa7ea8c93ec8b9ead17`  
		Last Modified: Tue, 12 May 2026 00:14:36 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da9a6de821e86987a2ca5296bb595ea51e476219cf4790ff5c86eb17685fbc2`  
		Last Modified: Tue, 12 May 2026 00:14:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed3f755582a10fbcd056588648deb556653b5bbbcbd6feab6f6004675540c7e`  
		Last Modified: Tue, 12 May 2026 00:14:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3a4f7544ce7f369b2efd28fe8eb708732e1b37a4b61b2b8b7d361d220c6ab3`  
		Last Modified: Tue, 12 May 2026 00:14:38 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891aa07eca0a343d8087ad9f3ef8457decd609904ca7fe0b43f8223bda0336aa`  
		Last Modified: Tue, 12 May 2026 00:14:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4652d7c8792bfbf917a9394b85d05df17d0fd07464eacbfbecd16a9d2beec0a5`  
		Last Modified: Tue, 12 May 2026 00:14:39 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c843e56f4e104408ccac218932817f572d9bec12b1761b64e659642416f8f1`  
		Last Modified: Tue, 12 May 2026 00:14:39 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b654619875119157d125db7ccc67c74850467aee78d1ddd6363b5a5c63974bd4`  
		Last Modified: Tue, 12 May 2026 00:14:40 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:e02d459c52c1e6daefa32c63766254d6dc6764cf0b60483036bde083f01d7065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5865074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9761aa8343b6fa44997dda13403a08f5f718c9360c8aa03e7fec0f58053dd4`

```dockerfile
```

-	Layers:
	-	`sha256:b58f10ea3eeaa07e52199a795c99e70f89031055b8418c5840761daf415db2fe`  
		Last Modified: Tue, 12 May 2026 00:14:35 GMT  
		Size: 5.8 MB (5821849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7c32ab676a1ffb7d669f2a336a3387fa8697e4dfd001aadba978edd73faa63`  
		Last Modified: Tue, 12 May 2026 00:14:34 GMT  
		Size: 43.2 KB (43225 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:005e1e5c8735f067ec0bf5faf73578871b86fba6c6bbe7f3d9d54d1df9082aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.1 MB (473054049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71af5affa46cb19025ee3ff88d9b42f69670dcbd38bbcd076f3fb44088f562d7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 11 May 2026 01:10:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:04 GMT
ENV container oci
# Mon, 11 May 2026 01:10:05 GMT
COPY dir:f96b78a7f24437106ae6a323adf2c06c98f78157637998e58adf24d336fc59f9 in /      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:05 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:50Z" "org.opencontainers.image.created"="2026-05-11T01:09:50Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:50Z
# Tue, 12 May 2026 00:07:04 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 May 2026 00:07:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 May 2026 00:13:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 May 2026 00:13:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 00:13:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 May 2026 00:13:55 GMT
RUN fc-cache -v # buildkit
# Tue, 12 May 2026 00:13:55 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2026 00:13:55 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 May 2026 00:13:55 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 00:13:55 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:13:55 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 May 2026 00:13:55 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 May 2026 00:13:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 May 2026 00:13:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 May 2026 00:13:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 May 2026 00:13:57 GMT
LABEL org.label-schema.build-date=2026-04-22T11:33:27.171Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=49d42f259436b65ab5297f19a65855bed082f302 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.4 org.opencontainers.image.created=2026-04-22T11:33:27.171Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=49d42f259436b65ab5297f19a65855bed082f302 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.4
# Tue, 12 May 2026 00:13:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 May 2026 00:13:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 00:13:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 May 2026 00:13:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 May 2026 00:13:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8145827b8d0d0740e92d2e089fbcb978a627f59c38b982f607785cb610c96650`  
		Last Modified: Tue, 12 May 2026 00:15:05 GMT  
		Size: 19.5 MB (19466578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:debee9562fef1eddc42d41ab7bab0dbbc03e39204bef2e2255a95d1c9f978039`  
		Last Modified: Tue, 12 May 2026 00:15:12 GMT  
		Size: 398.8 MB (398825061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858d3bb03b1d788c271d1642390f38c9f71d853e3a7877ec5d709179b4ad2cfc`  
		Last Modified: Tue, 12 May 2026 00:15:04 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f4fb4265d92523fbe1b9dcb0e332471675798c98d1bbd1e3ad4e909ae2ec03`  
		Last Modified: Tue, 12 May 2026 00:15:05 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6381b07986571d72e434f1e01649935c9de718815bb611fcd01e4c87b6b1b64b`  
		Last Modified: Tue, 12 May 2026 00:15:05 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678d3d6325b3c24f7ef1e78f75bc97738b75e7a0785465bb1712783b77c4ddbb`  
		Last Modified: Tue, 12 May 2026 00:15:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14f4d6a5e59e67d80216ae938214a6ed604e32d1750ad4288fa9370bc79db5e`  
		Last Modified: Tue, 12 May 2026 00:15:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4fc6cb7a4a60a1dd5d6597c24db8eec2369c566860c38afa99cd368edb85c`  
		Last Modified: Tue, 12 May 2026 00:15:06 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dc4d160828a1960c651652c4aa1d8e1376a0bb14650c1fe3413f9aeccfc8fb`  
		Last Modified: Tue, 12 May 2026 00:15:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059e45681f3337a1ef845797e6f384785330f0f00beb3ce0c5b3782e300dc5d3`  
		Last Modified: Tue, 12 May 2026 00:15:07 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4042009bdd5c6b229f93ba1db11f63c3ef644257d8478bc9ad00ed24d7e1f4`  
		Last Modified: Tue, 12 May 2026 00:15:08 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ae2a5aff1b9bdba0cc64b25cf90639f991d6b05f3b462caa9b7cd848a987e0`  
		Last Modified: Tue, 12 May 2026 00:15:09 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.4` - unknown; unknown

```console
$ docker pull kibana@sha256:f79895b5b22f8c994b4a04524cb7744fb9043c30bf6bab85444ca073f7b6f4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5864004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6f370d2e034dad3e5be6387344eac384140a796763b9416a88ceee9c65977e`

```dockerfile
```

-	Layers:
	-	`sha256:09c2e890092943137a4222f88591f715fcf3071289e9cab9196f609c78eaaf4c`  
		Last Modified: Tue, 12 May 2026 00:15:04 GMT  
		Size: 5.8 MB (5820521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79bb54b09b350c9a2d96753d69b12e867290fc6f5bd13c126d98fdcce19ca9a1`  
		Last Modified: Tue, 12 May 2026 00:15:04 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.0`

```console
$ docker pull kibana@sha256:c5dbafe0913bc401c49769f737fef9fd90ee4fbfe459dcf683885d81a529afff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.0` - linux; amd64

```console
$ docker pull kibana@sha256:e4af5726f26a4e3dba234e7db183b9eeb51cf21afafbcd0288051385a400aa2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.2 MB (528230052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41f41f3ba2eba66a5f5c0bf1e843f3ff7e5d6f5c7585734d6775873c19a2932`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 11 May 2026 01:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:07:55 GMT
ENV container oci
# Mon, 11 May 2026 01:07:56 GMT
COPY dir:d396e6c334ec17a1ba4a03f21481f526666f77d114978313ef1df55edd8e1412 in /      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:07:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:07:39Z" "org.opencontainers.image.created"="2026-05-11T01:07:39Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:07:39Z
# Tue, 12 May 2026 00:06:13 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 May 2026 00:06:13 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 May 2026 00:15:24 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 May 2026 00:15:25 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 00:15:25 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 May 2026 00:15:25 GMT
RUN fc-cache -v # buildkit
# Tue, 12 May 2026 00:15:25 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2026 00:15:25 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 May 2026 00:15:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 00:15:25 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:15:25 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 May 2026 00:15:25 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 May 2026 00:15:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 May 2026 00:15:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 May 2026 00:15:27 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 May 2026 00:15:27 GMT
LABEL org.label-schema.build-date=2026-04-30T16:38:11.955Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b2e39752e03b56f48f51943214475ddba1f8e974 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T16:38:11.955Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b2e39752e03b56f48f51943214475ddba1f8e974 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Tue, 12 May 2026 00:15:27 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 May 2026 00:15:27 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 00:15:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 May 2026 00:15:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 May 2026 00:15:27 GMT
USER 1000
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ebef1c49986232959a61f658914aaff2ff91e860bbc851521143e14c0bd8b5`  
		Last Modified: Tue, 12 May 2026 00:16:41 GMT  
		Size: 19.5 MB (19521621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3603cc8d4805767e477f1c7b6f9928fedf1413fd013054f44f8a9c136288617b`  
		Last Modified: Tue, 12 May 2026 00:16:51 GMT  
		Size: 452.2 MB (452155305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d350a3c1783be68be7e40ca3bafc432795f6fd77203e69b273250a180f9d398d`  
		Last Modified: Tue, 12 May 2026 00:16:39 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf72b5446e0a7d470392cd9c3b002f3597eb3f4621a90346e85a8d0095ee81a`  
		Last Modified: Tue, 12 May 2026 00:16:41 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e0874a0a8fd93040bbb0e71c4e4d97d61e74a3a62908f9a29453a14c0b610d`  
		Last Modified: Tue, 12 May 2026 00:16:41 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bb4a3dedd1e78c0ce667627a7620a7b15fae355533fc1aacaaf3c07bd68eae`  
		Last Modified: Tue, 12 May 2026 00:16:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08421f2ea8b14e6e798b6fea4d4c32638f2fe7cb3545b424f82088c6ce0b2139`  
		Last Modified: Tue, 12 May 2026 00:16:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef2d74a834ccc532d8a02ee67cff8f6d85b33abf5444ed5a1b504efe86d40a`  
		Last Modified: Tue, 12 May 2026 00:16:43 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b14f97722a612e43a8eec0642d472ddaeac2d5b412a91d0b1b43afbaca45c9`  
		Last Modified: Tue, 12 May 2026 00:16:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690310e92f95f02f7e8eea0fe39e3d8aeaf5d16a839262994bc52f0ff560b1a7`  
		Last Modified: Tue, 12 May 2026 00:16:44 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84052afba97c59333da98e928ab1cdad5e338ef8e3eb859a61b5e4247d232fb5`  
		Last Modified: Tue, 12 May 2026 00:16:44 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f4900330b2f59d32026aa741042c12affb4068a16a3d97f240cad23ba95afa`  
		Last Modified: Tue, 12 May 2026 00:16:45 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.0` - unknown; unknown

```console
$ docker pull kibana@sha256:f4f1aece23c8924d29c160779fb79df09acd59a50cfe977d62cb9df202c4f44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db592a302bc8e45fe528a29a444f8d4989a03afb5318f0a6610aebcce84cbd60`

```dockerfile
```

-	Layers:
	-	`sha256:e38181ba45db0a7c1dc98bcc802ae76516365425993d1d3683239035af5db4d9`  
		Last Modified: Tue, 12 May 2026 00:16:40 GMT  
		Size: 5.9 MB (5884420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0588ef7f5a0630f23d94c4d3ab3df90d07f2fb4927bcf34d8ecb4f1c0eead33e`  
		Last Modified: Tue, 12 May 2026 00:16:39 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:879687bd50dad9300b9c24ca5072c6d967d38da69adebbb573491c466a766fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539233325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6824a7dcbd04d9285d75d8d1ee00e6c7ca4b5beca0d0312575e307c9086368`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 11 May 2026 01:10:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:04 GMT
ENV container oci
# Mon, 11 May 2026 01:10:05 GMT
COPY dir:f96b78a7f24437106ae6a323adf2c06c98f78157637998e58adf24d336fc59f9 in /      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:05 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:50Z" "org.opencontainers.image.created"="2026-05-11T01:09:50Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:50Z
# Tue, 12 May 2026 00:07:03 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 May 2026 00:07:03 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 May 2026 00:14:31 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 May 2026 00:14:32 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 00:14:32 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 May 2026 00:14:32 GMT
RUN fc-cache -v # buildkit
# Tue, 12 May 2026 00:14:32 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2026 00:14:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 May 2026 00:14:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 00:14:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:14:33 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 May 2026 00:14:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 May 2026 00:14:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 May 2026 00:14:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 May 2026 00:14:35 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 May 2026 00:14:35 GMT
LABEL org.label-schema.build-date=2026-04-30T16:38:11.955Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b2e39752e03b56f48f51943214475ddba1f8e974 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.0 org.opencontainers.image.created=2026-04-30T16:38:11.955Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b2e39752e03b56f48f51943214475ddba1f8e974 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.0
# Tue, 12 May 2026 00:14:35 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 May 2026 00:14:35 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 00:14:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 May 2026 00:14:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 May 2026 00:14:35 GMT
USER 1000
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde11339375cde08043eee21a92662ad3fa103fe2300b0ae99b89da01df7be6`  
		Last Modified: Tue, 12 May 2026 00:15:54 GMT  
		Size: 19.5 MB (19466573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a719c5918d75e24fa235c3e0585b7dfac79ca043891cd13e835a037f95ed5c8`  
		Last Modified: Tue, 12 May 2026 00:16:06 GMT  
		Size: 465.0 MB (465004341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784ed1882a40dfdbcaca0f950b683c25bb004acecc26ccb371bee8fd804facc1`  
		Last Modified: Tue, 12 May 2026 00:15:52 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b8980a93ab850c954327fcbad6654b3143fa6a821fb6f903818946cdd8a4b`  
		Last Modified: Tue, 12 May 2026 00:15:54 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0a777ec53f3396c2649800dd1007721ca059c8714b7ba923ed8e4923a9b900`  
		Last Modified: Tue, 12 May 2026 00:15:54 GMT  
		Size: 5.2 KB (5233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575418861868613902f0bef7a89160df752986fad0d87334f4128b599385a62c`  
		Last Modified: Tue, 12 May 2026 00:15:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cada46841f2a654ddf68a67cf2a988e8998aac22ce34111d01457dabe48bf4`  
		Last Modified: Tue, 12 May 2026 00:15:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47edaf045067cd019ddc7a06cee82eec2ad131a541b6cf28b069ead7e5c906fe`  
		Last Modified: Tue, 12 May 2026 00:15:56 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4211da3f82554958811fd7a1edc833e7514316ed147d0eeac9fe39f3208f3`  
		Last Modified: Tue, 12 May 2026 00:15:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0327d9d8f40cdd566862e843ebfea037dc691bcdda4268a7519a2d7c732f0b`  
		Last Modified: Tue, 12 May 2026 00:15:57 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df520ddc1a6f775c17b0f9b37ad42eb2ab076dc29cd28abdca80e1f75137020c`  
		Last Modified: Tue, 12 May 2026 00:15:58 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee68594cee1b4a5f3458c7f499e9c31576b39276a48a31b0d8e4f97570e8090`  
		Last Modified: Tue, 12 May 2026 00:15:58 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.0` - unknown; unknown

```console
$ docker pull kibana@sha256:8ea2874732f1ddd1adb0f717000ff6604d9aa6c60e84a8af8cd66e6a02b524e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9506f32d860cd3ce9fff6ebb7a9e9caca3be8809c39cf5249199dbf17883e2`

```dockerfile
```

-	Layers:
	-	`sha256:740d8a06b2c6843e2411144fe7adedd91225c9a5a3343be175ee5b64d38428f9`  
		Last Modified: Tue, 12 May 2026 00:15:53 GMT  
		Size: 5.9 MB (5883092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b79b953e871099b717219e49728a46674c954825bda866fd4282914e03708a`  
		Last Modified: Tue, 12 May 2026 00:15:52 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
