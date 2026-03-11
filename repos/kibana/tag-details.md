<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.12`](#kibana81912)
-	[`kibana:9.2.6`](#kibana926)
-	[`kibana:9.3.1`](#kibana931)

## `kibana:8.19.12`

```console
$ docker pull kibana@sha256:6138d6457e25ba8a06203cd4939879d77ce333078bcc630450666af412e10c68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.12` - linux; amd64

```console
$ docker pull kibana@sha256:1d8b7245ff3f5856dde5e389a37e8220e713f36064e25ec16a36ab5065f15188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442059519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e9ef33c4c8b5cdb53e2bfc5744c89ea823e72a4577fc0c119f0ffac72989c0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:03:05 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Feb 2026 19:03:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:20:25 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Feb 2026 19:20:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:20:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Feb 2026 19:20:26 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Feb 2026 19:20:26 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Feb 2026 19:20:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Feb 2026 19:20:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:20:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:20:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Feb 2026 19:20:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:20:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
LABEL org.label-schema.build-date=2026-02-24T03:15:27.497Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a2a93735478172a315d2ced4aded3024cc029648 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-24T03:15:27.497Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a2a93735478172a315d2ced4aded3024cc029648 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Thu, 26 Feb 2026 19:20:28 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Feb 2026 19:20:28 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Feb 2026 19:20:28 GMT
USER 1000
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c37632575b0f4979ab33f7e579bc1afe6b8b7834b531bec71fc89b0b6586b2`  
		Last Modified: Thu, 26 Feb 2026 19:21:24 GMT  
		Size: 9.4 MB (9433908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f8f799cfb274e3c1bbc295a4997a240568b5b07638bda8d2caaca4b624bfe0`  
		Last Modified: Thu, 26 Feb 2026 19:21:31 GMT  
		Size: 386.3 MB (386254274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13107af030972ccabfe50cecd33704ab2ffd1d3f1a81ea648f8254e2a41e308`  
		Last Modified: Thu, 26 Feb 2026 19:21:23 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b743ca35d0cc3fe721979cb977ddabf79da9a095133bc5333a76a0854d6258`  
		Last Modified: Thu, 26 Feb 2026 19:21:24 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d8ae5003a11d2bf2a83ce1d773f6e7fbdc2577c7bdff802009caa8cd809f04`  
		Last Modified: Thu, 26 Feb 2026 19:21:24 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb070a0385c82d22f013286b522f7aeea6f58fadd7c59f53fcdc713900a7005`  
		Last Modified: Thu, 26 Feb 2026 19:21:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d25ca7c9f2933bfb53e6b19729aec45de8a85cb57acc5550237a210cbc15a6`  
		Last Modified: Thu, 26 Feb 2026 19:21:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3d9ded5d3e10893cad8950ac7acf83ac6f227b49363ec0be4154973e2fe9fa`  
		Last Modified: Thu, 26 Feb 2026 19:21:25 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce94af364e2f606f0e1bce1e5aaa9cb76dc12736532e5840a69bb74974a7447`  
		Last Modified: Thu, 26 Feb 2026 19:21:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b754ef96fb78cc074ce6f25e1b03617b4420b6683aae51a0a7bb9adef02e90`  
		Last Modified: Thu, 26 Feb 2026 19:21:26 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609312eb9ee2ec9ab70dcfae0292a6df5551176489ee12da4a3eff64d5ee7121`  
		Last Modified: Thu, 26 Feb 2026 19:21:26 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.12` - unknown; unknown

```console
$ docker pull kibana@sha256:68f8356e80861aa4d1d826b28a249921f9ee7b90753caf2289ba6ff496f387d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930b36645bc6286e2ffc51fba5f8201863df0234010c030901c68fe077418f2c`

```dockerfile
```

-	Layers:
	-	`sha256:6d2dadd3644bfb9164d3f4c3b4d611d0f23957179cf32b4caad0d3389d5df30a`  
		Last Modified: Thu, 26 Feb 2026 19:21:23 GMT  
		Size: 4.9 MB (4921967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee6f1c175fe286f9111f0c86a91ae9614ffbae141768995403604ced572402b`  
		Last Modified: Thu, 26 Feb 2026 19:21:23 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.12` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:cc9ff12a908adef70edd48eec27a21669615ada792272abea19f3eb40a14d3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.0 MB (454963311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c0261e212f241b82b7d76507cbbc4d7605aaad6b96170ad68b6a8d99c30f2a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:02:45 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Feb 2026 19:02:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Feb 2026 19:17:46 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Feb 2026 19:17:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:17:46 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Feb 2026 19:17:46 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Feb 2026 19:17:46 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Feb 2026 19:17:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Feb 2026 19:17:46 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:17:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:17:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Feb 2026 19:17:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:17:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Feb 2026 19:17:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Feb 2026 19:17:48 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Feb 2026 19:17:48 GMT
LABEL org.label-schema.build-date=2026-02-24T03:15:27.497Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a2a93735478172a315d2ced4aded3024cc029648 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-24T03:15:27.497Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a2a93735478172a315d2ced4aded3024cc029648 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Thu, 26 Feb 2026 19:17:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Feb 2026 19:17:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Feb 2026 19:17:48 GMT
USER 1000
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be77a3b3a5eefe11bde3afe7849aca15bb9e51f2d01087b5ab07efd4449f293`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 9.5 MB (9451008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2769982df81b1475e8760b058c4d717c51d4b6ac058ad49de2870d07263506`  
		Last Modified: Thu, 26 Feb 2026 19:19:01 GMT  
		Size: 400.0 MB (400007369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340bfb2f0f1a9f02b2e097db61c5875a0200f54b61dcb1d06511efb075a5481f`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2f851b34cf728bddf474a8238aaa0fe69c63ff6ef71d1daa60601e2abed6c5`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70899995b124b9dac19e2dc2facddb6c1f4fd3f9f15648f20e9ab8dd3fb57832`  
		Last Modified: Thu, 26 Feb 2026 19:18:54 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16777e79b1d8f5a2604600eaaaff7e680c4b7d780d2916a2f2d4f41f5873a7cc`  
		Last Modified: Thu, 26 Feb 2026 19:18:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01297b2ded8d7d587bd2f090dee1475b910bed4b7887f4a67e250b780416bc6f`  
		Last Modified: Thu, 26 Feb 2026 19:18:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce79e306abd4b0874dfc266e497b361db9f7dd9ea77fe26a9db28c99849ca2b`  
		Last Modified: Thu, 26 Feb 2026 19:18:55 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e20f70fd4689df46f940500f29f9b3295fd4b0342327abb7568bf2340493f6`  
		Last Modified: Thu, 26 Feb 2026 19:18:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5ddfde7c4b07ebc314aab101c8c24c913d9605244fa6f58bb20094322ba72c`  
		Last Modified: Thu, 26 Feb 2026 19:18:56 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608c7cc31a49868dda121989e1b6881a65d57dd3d71620ea6485cfc1bcb86fe6`  
		Last Modified: Thu, 26 Feb 2026 19:18:56 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.12` - unknown; unknown

```console
$ docker pull kibana@sha256:0db04db01550bf0d26e81eafb5fbe645d1009556ed9f35fd1c5b9649d1678445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4964193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fe16c11a171a73a85ceef9f7ef2f281340215c209468620009a6a814fa4f38`

```dockerfile
```

-	Layers:
	-	`sha256:6bacfce476a00ea06cb451c675d29200947188ceeb2baec28360cbb5bd014411`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 4.9 MB (4923031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9083dcd49361a0f45e8a56e239687cc582e05dbccd736f2b09fa12d56e70b6`  
		Last Modified: Thu, 26 Feb 2026 19:18:53 GMT  
		Size: 41.2 KB (41162 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.6`

```console
$ docker pull kibana@sha256:6d9362c40bac8152733c3a83d255bb5f034042ecf45e14e85e4b221856234114
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.6` - linux; amd64

```console
$ docker pull kibana@sha256:723aeb9af62d3b4db0aefae030f79a8de4f52fb3e6bce1fc4233e4e174858d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448493735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd91ea40594fae9fe1d469e4c716a29531821f58472dabc22609916fe0cf74e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:37:26 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 11 Mar 2026 18:37:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:46:28 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 11 Mar 2026 18:46:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:46:29 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 11 Mar 2026 18:46:29 GMT
RUN fc-cache -v # buildkit
# Wed, 11 Mar 2026 18:46:29 GMT
WORKDIR /usr/share/kibana
# Wed, 11 Mar 2026 18:46:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 11 Mar 2026 18:46:29 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:46:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:46:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 11 Mar 2026 18:46:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:46:30 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 11 Mar 2026 18:46:31 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 11 Mar 2026 18:46:31 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 11 Mar 2026 18:46:31 GMT
LABEL org.label-schema.build-date=2026-02-24T03:41:47.441Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-24T03:41:47.441Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Wed, 11 Mar 2026 18:46:31 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 11 Mar 2026 18:46:31 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:46:31 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 11 Mar 2026 18:46:31 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 11 Mar 2026 18:46:31 GMT
USER 1000
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b0340e7f7f742e002531fb33eba0dc8d7c9ac5071e4d0c4b7e8b7c61dd5651`  
		Last Modified: Wed, 11 Mar 2026 18:47:29 GMT  
		Size: 19.5 MB (19530827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab90ef9786b53f8bbaeb38c53e10855bef6b1a8d281b70d1b5dc245b92495d79`  
		Last Modified: Wed, 11 Mar 2026 18:47:35 GMT  
		Size: 372.4 MB (372413620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969eeec7daed8131f285d6b9afa2c5b6650e7c3d6c85e8bc5d282d713795022a`  
		Last Modified: Wed, 11 Mar 2026 18:47:28 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cda2ec1c9a69626f0f35cdc321eb20fa85adf765855e42ccc133b7375468a7`  
		Last Modified: Wed, 11 Mar 2026 18:47:29 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb2ebc7489f0ee98bb8b649f83d39cfd22ba4bd0d56684a24c37e65be17205`  
		Last Modified: Wed, 11 Mar 2026 18:47:29 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6783018edb8ed9a7d97cc66bbbcfc15ec26dc80d6afb41da048449230dad859`  
		Last Modified: Wed, 11 Mar 2026 18:47:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d6cd40498f96482757b060f386282c25b5fb4115c8120160ca17a85c77b01f`  
		Last Modified: Wed, 11 Mar 2026 18:47:30 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5af192e38cdb9318c2503cd4f324789b552bc20360d31db4108120ddc98964`  
		Last Modified: Wed, 11 Mar 2026 18:47:31 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cc05935c6fe4a9275c735e1dc4bad3cf6661c5828fdb38b222dcdac46fd2f2`  
		Last Modified: Wed, 11 Mar 2026 18:47:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648cffd6a307536f9211ef3d098b6b2de6d68fbdd7440e671c6a1d52b52b37ce`  
		Last Modified: Wed, 11 Mar 2026 18:47:31 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d46cbb893d9f52fd65656759e1072caf30c4df3a7510cc9ec8e4a41d048496e`  
		Last Modified: Wed, 11 Mar 2026 18:47:32 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14d8d6c73ea342d30aa14d18c740fff2529223810a3bb82610b70367016436b`  
		Last Modified: Wed, 11 Mar 2026 18:47:32 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.6` - unknown; unknown

```console
$ docker pull kibana@sha256:1884a31a6d6ba4858a3fbc132a86d9286f7fe9c8a0d5313f4933af984bd35968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e633792239666cffe1b875b9a59bb043b90d5559096907ec5f62ec1792f4289`

```dockerfile
```

-	Layers:
	-	`sha256:ed458e9b0db285a405e81ee64815b2a1334c4daf16492960e75beb8d43a7e2c6`  
		Last Modified: Wed, 11 Mar 2026 18:47:28 GMT  
		Size: 5.7 MB (5747620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f8a40c70f99d079936114281d24b253eac16089a6a538ad744c152567e0798`  
		Last Modified: Wed, 11 Mar 2026 18:47:27 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b03b8a2efc15cdd8bc0eb1a5d837b688d9d068b642f78a76e23b7ff3b7036137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.4 MB (460401036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e893951b2e4d97c72ed699d213db846a757da20e48f79175fa0bb1c239a6405a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:35:16 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 11 Mar 2026 18:35:16 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:42:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 11 Mar 2026 18:42:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:42:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 11 Mar 2026 18:42:51 GMT
RUN fc-cache -v # buildkit
# Wed, 11 Mar 2026 18:42:51 GMT
WORKDIR /usr/share/kibana
# Wed, 11 Mar 2026 18:42:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 11 Mar 2026 18:42:51 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:42:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:42:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 11 Mar 2026 18:42:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:42:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 11 Mar 2026 18:42:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 11 Mar 2026 18:42:53 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 11 Mar 2026 18:42:53 GMT
LABEL org.label-schema.build-date=2026-02-24T03:41:47.441Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-24T03:41:47.441Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Wed, 11 Mar 2026 18:42:53 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 11 Mar 2026 18:42:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:42:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 11 Mar 2026 18:42:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 11 Mar 2026 18:42:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12d74bddd103335b5ac9fb08d2f5a6279bc0611533d7fca8525472c18af21de`  
		Last Modified: Wed, 11 Mar 2026 18:44:00 GMT  
		Size: 19.5 MB (19482110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243753f10150cb51c1895f70984a3a571f127c41efaa382355140a150abfe9a0`  
		Last Modified: Wed, 11 Mar 2026 18:44:07 GMT  
		Size: 386.2 MB (386156586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59df0be9dcfb995e6b7eb6e609df370f1af624e2b1fb5afaaafdac8f1ef3d8c5`  
		Last Modified: Wed, 11 Mar 2026 18:43:59 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996fed34f9a25d30bb02e70169f2ae27045d4250e06cf596a0d2a14a8c1d2272`  
		Last Modified: Wed, 11 Mar 2026 18:44:00 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e03b23354206a866b73312a92e85ce5c80c76ec367d9e7fc2cc4ee09fd4e47`  
		Last Modified: Wed, 11 Mar 2026 18:44:00 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c3170721ef0fab34978dcf5ef726e700b3532611ea024c1cc518063c23222`  
		Last Modified: Wed, 11 Mar 2026 18:44:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b01d22313b9352ccaac3b7b5f10762dbbfd2c2468799be2f30943aba4799d8`  
		Last Modified: Wed, 11 Mar 2026 18:44:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc00924023061130fe4c2345f1fda8e1581e96361a76902cc935e509319eaa`  
		Last Modified: Wed, 11 Mar 2026 18:44:02 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9c1843ce4297e85d9c0ef61aa945d29f20ddbe9fc7923ca2999cdb25a26194`  
		Last Modified: Wed, 11 Mar 2026 18:44:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd89a888f1b314f73fc12cc66be0a73c662f309c87d0f0e45cbdb1f180a68fc4`  
		Last Modified: Wed, 11 Mar 2026 18:44:03 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5c62f867b47f0edf546caeed862b9d9a53b2c80ed236d558b017b3bd21f33`  
		Last Modified: Wed, 11 Mar 2026 18:44:03 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11cd5182d34dbc69e6e77eb36c15f6e7d926e4e2dc89f5859f66607e9ec8da3`  
		Last Modified: Wed, 11 Mar 2026 18:44:04 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.6` - unknown; unknown

```console
$ docker pull kibana@sha256:45a8959e5683a7b26f85bbec1379997a8d76ade76ccc77c68a9d57dd974b81ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775cbcce6452c8661cce9928e11d66e63f47e4685989557a53a43fd8f18555a6`

```dockerfile
```

-	Layers:
	-	`sha256:3c7f684ff72e7a498677c7d837df558a3bfbfed9faf1cd48dd0e9614f5bcc597`  
		Last Modified: Wed, 11 Mar 2026 18:43:59 GMT  
		Size: 5.7 MB (5746292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35856c9467846edf86b63fa491aafdd4ce12f656739823fe73e3f10075537b53`  
		Last Modified: Wed, 11 Mar 2026 18:43:59 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.1`

```console
$ docker pull kibana@sha256:0c93f1689907b7c09843945cf2b0863c34af5e8be966d288249cb32121f95910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.1` - linux; amd64

```console
$ docker pull kibana@sha256:51db04a6fde780b9f5384d0d97fbcc3f3670f1706c07caac232da5083d75d9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453375753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca9bae9aa896ffbdc696bcfd528b20a90a70fe3dbd6b6a6fc6601fc39b6c767`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:35:21 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 11 Mar 2026 18:35:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:44:58 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 11 Mar 2026 18:44:59 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:44:59 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 11 Mar 2026 18:44:59 GMT
RUN fc-cache -v # buildkit
# Wed, 11 Mar 2026 18:44:59 GMT
WORKDIR /usr/share/kibana
# Wed, 11 Mar 2026 18:44:59 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 11 Mar 2026 18:44:59 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:44:59 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:44:59 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 11 Mar 2026 18:44:59 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:45:00 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 11 Mar 2026 18:45:01 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 11 Mar 2026 18:45:01 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 11 Mar 2026 18:45:01 GMT
LABEL org.label-schema.build-date=2026-02-24T03:42:25.053Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=342266a63c5cedf139febf5a982ceb9a1c46690b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-24T03:42:25.053Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=342266a63c5cedf139febf5a982ceb9a1c46690b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Wed, 11 Mar 2026 18:45:01 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 11 Mar 2026 18:45:01 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:45:01 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 11 Mar 2026 18:45:01 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 11 Mar 2026 18:45:01 GMT
USER 1000
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506979eb1ec666ff201964d43cf86c75046e338e5767f5aeb8c15875b784a7c3`  
		Last Modified: Wed, 11 Mar 2026 18:45:58 GMT  
		Size: 19.5 MB (19530680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af1fddcc7b2ad636f0eda91f85e8451b69944c4f9a1d6f4c3b3cbdedb4c2fff`  
		Last Modified: Wed, 11 Mar 2026 18:46:05 GMT  
		Size: 377.3 MB (377295776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67502edd7408cc41b436ae8661bd1c660ec3a9721757a4949caa2e865d4c7a8`  
		Last Modified: Wed, 11 Mar 2026 18:45:56 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fe338ccf9c584cba14744c6ee753cf1723d686c98429f45b9ede5115b6e99`  
		Last Modified: Wed, 11 Mar 2026 18:45:58 GMT  
		Size: 16.5 MB (16460482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aba5a61b4bf2f9dac2e2b12f23fe864002d2080fd282cc3dc85ab455ea1b1a6`  
		Last Modified: Wed, 11 Mar 2026 18:45:57 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59c2311bad5a68306cae093aa9210164c48bc5029c47910a063182f59e1f061`  
		Last Modified: Wed, 11 Mar 2026 18:45:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d2a73e8e4013b91f44d81ab7d472defa07a2adff29cd4d29875e840f32f64`  
		Last Modified: Wed, 11 Mar 2026 18:45:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea254a764d92492d810e362f4d6b340e7222a2d8589d4e85ef033ed841b127e1`  
		Last Modified: Wed, 11 Mar 2026 18:45:59 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3df7b971af29fd6d5d99432fc413227ee3fffef1aad7bbe1872a8c1ceb2370`  
		Last Modified: Wed, 11 Mar 2026 18:46:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859aa3f3421386fb4995b443a2f34ea80d1946abcec83cfb960bcbd809db0db1`  
		Last Modified: Wed, 11 Mar 2026 18:46:00 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2138ed7859b631463bc3d9d2c71a418bad086ecd500ec10995dabc9789bb364`  
		Last Modified: Wed, 11 Mar 2026 18:46:01 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd05473ff3026ac30e093d6a2a4d4c88aed5d6851271976b8689dbca78a32248`  
		Last Modified: Wed, 11 Mar 2026 18:46:01 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.1` - unknown; unknown

```console
$ docker pull kibana@sha256:ad7c484579bb3bb77fadc7fa6c9c0023162178e41474ecfe8e6ccdd10fa2be65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927cdf7b07134618d0870977186e2323ea0c1261425d05f2a12314716d854d1b`

```dockerfile
```

-	Layers:
	-	`sha256:cc82b2ed956c168b52ae95005373de49f0072506033d5add23e3327274367d74`  
		Last Modified: Wed, 11 Mar 2026 18:45:57 GMT  
		Size: 5.8 MB (5813739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e91e9327da226ae1779e3c672b5e26d3c77033eeb66c5a60736f9c564cb76c0`  
		Last Modified: Wed, 11 Mar 2026 18:45:56 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1c82217432dc286f62d2bca62516aabb512bd6ddd2cf0c426e2a50eab4c26271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.3 MB (465269844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bdb1ed802a04f24d0bd363ebbbe12df8e3153fba10e489070d920ecf371d1b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:36:14 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 11 Mar 2026 18:36:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:44:06 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 11 Mar 2026 18:44:06 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 11 Mar 2026 18:44:07 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 11 Mar 2026 18:44:07 GMT
RUN fc-cache -v # buildkit
# Wed, 11 Mar 2026 18:44:07 GMT
WORKDIR /usr/share/kibana
# Wed, 11 Mar 2026 18:44:07 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 11 Mar 2026 18:44:07 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:44:07 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:44:07 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 11 Mar 2026 18:44:07 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:44:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 11 Mar 2026 18:44:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 11 Mar 2026 18:44:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 11 Mar 2026 18:44:09 GMT
LABEL org.label-schema.build-date=2026-02-24T03:42:25.053Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=342266a63c5cedf139febf5a982ceb9a1c46690b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-24T03:42:25.053Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=342266a63c5cedf139febf5a982ceb9a1c46690b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Wed, 11 Mar 2026 18:44:09 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 11 Mar 2026 18:44:09 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 11 Mar 2026 18:44:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 11 Mar 2026 18:44:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 11 Mar 2026 18:44:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edb5ed6d676188a38dc2365844807f6282fdc810a8e995b317b3570541d9c59`  
		Last Modified: Wed, 11 Mar 2026 18:45:14 GMT  
		Size: 19.5 MB (19482048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1effeafc2d3bc1523710e4c104ded717548dcea6f58ac16cf3341a344e063d2`  
		Last Modified: Wed, 11 Mar 2026 18:45:21 GMT  
		Size: 391.0 MB (391025446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e073e1ea64953512f8396e6cfa67fd4244e438865999556b2c92dfe04cb3390`  
		Last Modified: Wed, 11 Mar 2026 18:45:13 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedf2b84e31168c62d6400432aa6bb7bccc3ccc96859d00dd70e58d4193e6125`  
		Last Modified: Wed, 11 Mar 2026 18:45:14 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e34b7aafe87c838fec99cb8b16b04af75dd0217eb336d734c7cf92fb2cbed4`  
		Last Modified: Wed, 11 Mar 2026 18:45:14 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67179159330c9821739bead7bf7d0e89da8105a7ef07f0bea6ea50f92621067c`  
		Last Modified: Wed, 11 Mar 2026 18:45:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdecc391fdd2e891251bbed6da5025a765c76139355318d06916215c91331d7`  
		Last Modified: Wed, 11 Mar 2026 18:45:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998cce71fa48eabaac5e83330184a7896e7d6a5a6bb46d1980cac247c8a20632`  
		Last Modified: Wed, 11 Mar 2026 18:45:16 GMT  
		Size: 4.9 KB (4915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db108d178eae21dbf70595416923196b5ca34bc09dbbe861e6831cb9968caad1`  
		Last Modified: Wed, 11 Mar 2026 18:45:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c566b2411a3ae1e8318bb79bf1d7a13f3c6ddff6070e82502068f387f52ede5f`  
		Last Modified: Wed, 11 Mar 2026 18:45:17 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b29383376bca1b7fa88778212b24b6ace694fee285eceb826b61ff1aa6555e8`  
		Last Modified: Wed, 11 Mar 2026 18:45:17 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a3e9f8c3c78149aa5f38ed353ce35abcd8dc2e72eeb4bf712cea1846aac87f`  
		Last Modified: Wed, 11 Mar 2026 18:45:18 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.1` - unknown; unknown

```console
$ docker pull kibana@sha256:53ad4fb6e561d00ea762c3dc06ad6993eaaa741eebf80cf686aabd9c2c825dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d1d26d96fb7ee98baa2a31bd54146247f289581889253eb6a595a801304629`

```dockerfile
```

-	Layers:
	-	`sha256:ea272c3666d719b3064a7a15a5a948eb5f23d50aa75afe42042669489b1abdf0`  
		Last Modified: Wed, 11 Mar 2026 18:45:13 GMT  
		Size: 5.8 MB (5812411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5daaa89db7780679c4e7fa37ac7edb99a5b032ff1175f3f6d8c3aedde8fcf25a`  
		Last Modified: Wed, 11 Mar 2026 18:45:13 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
