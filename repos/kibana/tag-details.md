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

## `kibana:9.4.1`

```console
$ docker pull kibana@sha256:1f03b29ceb843ea7ea699875ed3d6162c087af734e7dc4a8f5b764ad74669249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.1` - linux; amd64

```console
$ docker pull kibana@sha256:d88ad79276c8cd774eb70d9be7cc2dce6b76a27374419a172a70becbe34823d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.0 MB (529957996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd95649abdee915b006e2166dbe3db01166e2ebc7dd35e1c16e6f3944566e93`
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
# Tue, 12 May 2026 21:26:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 May 2026 21:26:29 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 May 2026 21:35:25 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 May 2026 21:35:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 21:35:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 May 2026 21:35:26 GMT
RUN fc-cache -v # buildkit
# Tue, 12 May 2026 21:35:26 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2026 21:35:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 May 2026 21:35:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 21:35:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:35:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 May 2026 21:35:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 May 2026 21:35:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 May 2026 21:35:28 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 May 2026 21:35:28 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 May 2026 21:35:28 GMT
LABEL org.label-schema.build-date=2026-05-08T16:12:32.674Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T16:12:32.674Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1
# Tue, 12 May 2026 21:35:28 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 May 2026 21:35:28 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 21:35:28 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 May 2026 21:35:28 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 May 2026 21:35:28 GMT
USER 1000
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4fc14c8ddcf272b80a96d223b2787d12cecef4e725868b718b0a67ff55ab91`  
		Last Modified: Tue, 12 May 2026 21:36:43 GMT  
		Size: 19.5 MB (19521874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a85da1f2bdfe119eb98e110265f1ef5871d031c5957ad472d604a286c8ca7`  
		Last Modified: Tue, 12 May 2026 21:36:51 GMT  
		Size: 453.9 MB (453882991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c6f08d956c22165888f4cf54c2e179fcd8ac492665b9f44c47673b0ddb08ca`  
		Last Modified: Tue, 12 May 2026 21:36:42 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31497c82507ed494ad9c466321556d76c538a80373fac03ffc09d70f7d256e3b`  
		Last Modified: Tue, 12 May 2026 21:36:43 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342cc1e0013c36a9a1ebb1f9235c1611a5f1b189e6e03d547c1cb555c4ccc28c`  
		Last Modified: Tue, 12 May 2026 21:36:43 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ab0ccb61fed01d301c978a400d99e52b7eaa072f35cb23dadcb7da238ab2f6`  
		Last Modified: Tue, 12 May 2026 21:36:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6258a6b197e64299459dfd21db461493201f22161c8da3200648b50dcd8219`  
		Last Modified: Tue, 12 May 2026 21:36:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e20ddbfafaacfafb73f1526d1cd87f0c08ade9ce39fcbeeeca284df34dac7`  
		Last Modified: Tue, 12 May 2026 21:36:45 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b1c0f89f0a5ac0a0e2e43d8db7a999748995e7e5ebcf7d26c10081a58b7ee0`  
		Last Modified: Tue, 12 May 2026 21:36:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b55c9725ce64c9410b7dcdd662ef9cfad59cb7a9aaf1229f51c3c3e81bda4f`  
		Last Modified: Tue, 12 May 2026 21:36:46 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc17b275a1b39937894b9221a6dc85b14ab4c8348e857dcce0a9eed7a81be5e8`  
		Last Modified: Tue, 12 May 2026 21:36:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50800f4b8ca80efddecd4e215db8ef292eb2065842bca4ef4a708fc8b572c01`  
		Last Modified: Tue, 12 May 2026 21:36:47 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.1` - unknown; unknown

```console
$ docker pull kibana@sha256:f69a57e9c96d8b1becfea7775a2b82136b5e679d80d6f4d69cfc3a10c51903fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54481ef63b7917e15693eb0cc4e1cc4f6120b674d426329c2521605419fbba4f`

```dockerfile
```

-	Layers:
	-	`sha256:9195e7fea5df0ed0464eec8a41baf57ebe6a31de004eedaecd6f98382335eda1`  
		Last Modified: Tue, 12 May 2026 21:36:42 GMT  
		Size: 5.9 MB (5884286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9dfd7cc67ce158e147b8a2ebd220bc92ae713fbb9dfa872763a8e684554a12`  
		Last Modified: Tue, 12 May 2026 21:36:42 GMT  
		Size: 43.2 KB (43225 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:392eacb319103accec091e061092beda01cd8d43921dac58e846e11b40d9c506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.0 MB (540995883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4c09e9f6ec109a14d3ed6584897ecfd1d055faf4ab26360991f2e5cecb8262`
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
# Tue, 12 May 2026 21:26:39 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 May 2026 21:26:39 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 May 2026 21:33:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 May 2026 21:33:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 May 2026 21:33:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 May 2026 21:33:54 GMT
RUN fc-cache -v # buildkit
# Tue, 12 May 2026 21:33:54 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2026 21:33:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 May 2026 21:33:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2026 21:33:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:33:54 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 May 2026 21:33:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 May 2026 21:33:55 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 May 2026 21:33:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 May 2026 21:33:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 May 2026 21:33:56 GMT
LABEL org.label-schema.build-date=2026-05-08T16:12:32.674Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.1 org.opencontainers.image.created=2026-05-08T16:12:32.674Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6b92ccb460a725bd951d72bba6ead7b9697f9c6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.1
# Tue, 12 May 2026 21:33:56 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 May 2026 21:33:56 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 May 2026 21:33:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 May 2026 21:33:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 May 2026 21:33:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa38d7c0bb999818069f81aea2b0130b3d47413614732d77ea38b42d3712d1c`  
		Last Modified: Tue, 12 May 2026 21:35:15 GMT  
		Size: 19.5 MB (19466631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78db1d99bcd26205962213b7aadf47816cf08aee2a05a7a012b625cfc4d214f`  
		Last Modified: Tue, 12 May 2026 21:35:23 GMT  
		Size: 466.8 MB (466766849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e22d98d0453a42f73dd1a815c516d0c41e781693d59307b1270e20ffb411d8`  
		Last Modified: Tue, 12 May 2026 21:35:14 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b9ec0359943cf2dde2e20372c0c4b6888e0229a799eb3862d6af31c084cf4`  
		Last Modified: Tue, 12 May 2026 21:35:15 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62899781b7cd2218fbb295b8aadbd51bdab120c362dc3694e8a168472ac628f`  
		Last Modified: Tue, 12 May 2026 21:35:16 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c86772502c8f02546daab5d7e3c9c5efa21f06aabdd3ef9143a3fd2621ab3e`  
		Last Modified: Tue, 12 May 2026 21:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6199af73f6f986c963c8b1520459707084fc2fa82a9472f74a6cb625e26d49`  
		Last Modified: Tue, 12 May 2026 21:35:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103db04a71f7b5154e4d80a433488ca323829a3aa9ebb09e9c30c707afddeae1`  
		Last Modified: Tue, 12 May 2026 21:35:17 GMT  
		Size: 4.9 KB (4913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0cd66bfbd15bed6b8035070571e2a1714eef00a97bbc553914eaaf62d50136`  
		Last Modified: Tue, 12 May 2026 21:35:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc3e802108ee8625da895045451cd1625219a52ad2b73c66cde32211051c255`  
		Last Modified: Tue, 12 May 2026 21:35:18 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963108e26ee44599641e0b2443d1d7eab2a89415bea12ff0e16265695f6b91eb`  
		Last Modified: Tue, 12 May 2026 21:35:19 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37317105aed2d885a9e0c088c22e9de128221cb3e44d9495d131a365ad1b281`  
		Last Modified: Tue, 12 May 2026 21:35:20 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.1` - unknown; unknown

```console
$ docker pull kibana@sha256:118f79a866f968ba44a07e481c439be2cff98be5d9c4f22b7c1ea8eb095b3b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc569417704de5e151f514462b2de43e03aa4574a8aa6de1db8a117c3d3ba059`

```dockerfile
```

-	Layers:
	-	`sha256:100f0b3d65250616ea79a2d82f798da8fd15698305c7a2d65bb8d286c209475f`  
		Last Modified: Tue, 12 May 2026 21:35:14 GMT  
		Size: 5.9 MB (5882958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e96ae2ef3975e7f304b07f2f2e799d1d3ecff32d84418aea84d9f25ec616eaf`  
		Last Modified: Tue, 12 May 2026 21:35:14 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
