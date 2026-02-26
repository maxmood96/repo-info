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
$ docker pull kibana@sha256:ec0620240b359364b19849d2ef031151f7c193eef13559d276ea1134865977d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.6` - linux; amd64

```console
$ docker pull kibana@sha256:7674db0da78a0ed5e420df566526f7025cedc0175be51cbd451c59df78ef9975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448531624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ba46baa09fd829b56c9ebfc2031c9190d15c5c4727b03a884d7ef5afad2678`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 26 Feb 2026 19:03:10 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Feb 2026 19:03:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:19:37 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Feb 2026 19:19:37 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:19:37 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Feb 2026 19:19:38 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Feb 2026 19:19:38 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Feb 2026 19:19:38 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Feb 2026 19:19:38 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:19:38 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:19:38 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Feb 2026 19:19:38 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:19:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Feb 2026 19:19:39 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Feb 2026 19:19:39 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Feb 2026 19:19:39 GMT
LABEL org.label-schema.build-date=2026-02-24T03:41:47.441Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-24T03:41:47.441Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Thu, 26 Feb 2026 19:19:39 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 26 Feb 2026 19:19:39 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:19:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Feb 2026 19:19:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Feb 2026 19:19:39 GMT
USER 1000
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928bf6077cc13b76e089711becb1a5c7185fcb60efb066a13263c68dc242e482`  
		Last Modified: Thu, 26 Feb 2026 19:20:39 GMT  
		Size: 19.5 MB (19526025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf66f8a7749424a15c07c07c68bf18482a34e70143b79622b1e6da7735a2a2`  
		Last Modified: Thu, 26 Feb 2026 19:20:46 GMT  
		Size: 372.4 MB (372413598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726907f0b57322709de0e7f1ada16ce66809d97aaa5d5ce331a8b1c5cf6f6246`  
		Last Modified: Thu, 26 Feb 2026 19:20:38 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc587b3fa94e88b9658c9cea485ce9db8b1b2978d84124ec4f575a7a0efc8fa`  
		Last Modified: Thu, 26 Feb 2026 19:20:39 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5ccd929d7ee4accae6db1a23ff30419e109536b9431613d85074c92bcb474a`  
		Last Modified: Thu, 26 Feb 2026 19:20:39 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35039f8c8a607602cc36b0440f01fdb930a5f65a5be9d8d106970d931966a38`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c7bcdb61a6cbeb8ef86e4b951855cda92752d6ce3ba73d7c3c55a074c546db`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2c31d639c7ec52c6ed7b30a42040767ba5264bdbf043de32d44315eb2b4b12`  
		Last Modified: Thu, 26 Feb 2026 19:20:41 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b075fceeaef926bfb0e1144025cff1699a7b8a09aec129dbaefa971084bea52`  
		Last Modified: Thu, 26 Feb 2026 19:20:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3fd4580cca935cc97b623767fbcc32c11b2eda83cde3091ef6c8a1c2e339c2`  
		Last Modified: Thu, 26 Feb 2026 19:20:42 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc538afdc280555f6921f2a3dbef98947d6b5cd44ef43fc118449c6755bde7b7`  
		Last Modified: Thu, 26 Feb 2026 19:20:43 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb17b59dd726f185ba452d2fa859b3a79170eaa841b4320d62c8c3e2a625446`  
		Last Modified: Thu, 26 Feb 2026 19:20:44 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.6` - unknown; unknown

```console
$ docker pull kibana@sha256:794c51344f775b721c14695f764e8483b7f4d3dcdc06a0080f0b1b9b40edc768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a1efc2d6ddcb93159db5874d8423ee65c0cb35053d553cf2f3fa61f9ba253a`

```dockerfile
```

-	Layers:
	-	`sha256:8d8ae5632b518ffb8b91dded6bc7d7f9d3e200f45bea36833e13c2d1676a98df`  
		Last Modified: Thu, 26 Feb 2026 19:20:39 GMT  
		Size: 5.7 MB (5747598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041df50de4abc8ce6679a022aba11c8ad7ce66c190971c2054a1b631fd11092f`  
		Last Modified: Thu, 26 Feb 2026 19:20:38 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:22bc9b6ad62f1929d043161aea9534cb353d767941a5cf9ca9c1e413378d8d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.4 MB (460391722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de8f72e34c09c19b9e2a361f74357257b65631c3d9004325aefba0a78bb1453`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Thu, 26 Feb 2026 19:02:51 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Feb 2026 19:02:51 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:17:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Feb 2026 19:17:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:17:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Feb 2026 19:17:13 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Feb 2026 19:17:13 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Feb 2026 19:17:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Feb 2026 19:17:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:17:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:17:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Feb 2026 19:17:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:17:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Feb 2026 19:17:15 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Feb 2026 19:17:15 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Feb 2026 19:17:15 GMT
LABEL org.label-schema.build-date=2026-02-24T03:41:47.441Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-24T03:41:47.441Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3223f0953e9361aa0317520c49c8b4c3796cc4c3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6
# Thu, 26 Feb 2026 19:17:15 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 26 Feb 2026 19:17:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:17:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Feb 2026 19:17:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Feb 2026 19:17:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bb95b77137f0f4ea5aaee329244f6e002fe928cd32dc259eb67f81a6043f5a`  
		Last Modified: Thu, 26 Feb 2026 19:18:21 GMT  
		Size: 19.5 MB (19475656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d30bc4ffdcf746aad9f5bc0d8bad77ed8d8233e329c75789ea8b0ab6895c2`  
		Last Modified: Thu, 26 Feb 2026 19:18:30 GMT  
		Size: 386.2 MB (386156668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e16d5c065a27ce572472ffac123db8fb1df9318eeeb749c3d85fe95972f682d`  
		Last Modified: Thu, 26 Feb 2026 19:18:20 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d372c78e47e223536f93f14d802e9c475ad901667f22547c4c2d3942c3d1b4b`  
		Last Modified: Thu, 26 Feb 2026 19:18:21 GMT  
		Size: 16.5 MB (16460480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a310c525d44e9746eb15da8479dd153f2f2fbb2ac737b70b2a2f9238ef6f5f`  
		Last Modified: Thu, 26 Feb 2026 19:18:21 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6efdf1ddcdc406e5015dbef5f025d9f65c7e33f092ea6e2b7d381a0880c069e`  
		Last Modified: Thu, 26 Feb 2026 19:18:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe03644b9727d87256d033f619e9559ded13e41a79f1731a61a68a1998740b`  
		Last Modified: Thu, 26 Feb 2026 19:18:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb399802397fcd0712ace011379f31082c089029dad6057ed0d24f1d3014922`  
		Last Modified: Thu, 26 Feb 2026 19:18:23 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6cd73b3e2e8c272d7db9c1704ffc94b58cca9f37f19a10ad87b65cec174830`  
		Last Modified: Thu, 26 Feb 2026 19:18:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09025a05c14467d2683e2385004aacaf2bb633db0f0e8d4bf85263122de82b64`  
		Last Modified: Thu, 26 Feb 2026 19:18:24 GMT  
		Size: 73.4 KB (73447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ebf704829a7c3f7a42e7fd388eaf67ed4e7be50c59142aca89e35f5e6aff3d`  
		Last Modified: Thu, 26 Feb 2026 19:18:24 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed84a3db7ddd458058e421ab7c089ced4037c6b07e5f96368c4ac0633239e21`  
		Last Modified: Thu, 26 Feb 2026 19:18:25 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.6` - unknown; unknown

```console
$ docker pull kibana@sha256:c6964bffd9bc47fff6583b9424e3b1e7a545e7c41cbfb6a2de81abd827764962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25749902eed7830da99d10cfe3b19fc6cc9d824885d735ff0c1d3ab06b4c2247`

```dockerfile
```

-	Layers:
	-	`sha256:ed64d6f2d697880594ac14c0cb78b707d0b1e206486438b2da08628ed9e5df0d`  
		Last Modified: Thu, 26 Feb 2026 19:18:20 GMT  
		Size: 5.7 MB (5746270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7968ac11897cef759d1a340c717f256e20f59e3d40eb0f4a8c98efcfead421`  
		Last Modified: Thu, 26 Feb 2026 19:18:19 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.1`

```console
$ docker pull kibana@sha256:cceef6b8163b7f0cb12cc6519f8774ef6409552326cdb410f3a37d50d061e674
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.1` - linux; amd64

```console
$ docker pull kibana@sha256:5f1275f3d422ed9d9871c5f4fd235485ece12da3a713965f53d7eb036af45bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.4 MB (453414030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf203a8cef0942629084edbe9dd8ef875f2a39da02dca9f15732b5cab35c602`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Thu, 26 Feb 2026 19:03:09 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Feb 2026 19:03:09 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:20:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Feb 2026 19:20:28 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:20:28 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:20:28 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Feb 2026 19:20:28 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:20:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Feb 2026 19:20:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Feb 2026 19:20:30 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Feb 2026 19:20:30 GMT
LABEL org.label-schema.build-date=2026-02-24T03:42:25.053Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=342266a63c5cedf139febf5a982ceb9a1c46690b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-24T03:42:25.053Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=342266a63c5cedf139febf5a982ceb9a1c46690b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Thu, 26 Feb 2026 19:20:30 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 26 Feb 2026 19:20:30 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:20:30 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Feb 2026 19:20:30 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Feb 2026 19:20:30 GMT
USER 1000
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52030d1bbccdada3de70d1697199c0466c630043816cf521e4f4c478eff7c9fa`  
		Last Modified: Thu, 26 Feb 2026 19:21:33 GMT  
		Size: 19.5 MB (19526177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16289325849c22edc908e11bf96c0c3608e36da179d6fa0aee0e8a0520635ba`  
		Last Modified: Thu, 26 Feb 2026 19:21:49 GMT  
		Size: 377.3 MB (377295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41335df6605048f91c67377d2be5c7df6a45c8a80562f456fedc40a846a3c205`  
		Last Modified: Thu, 26 Feb 2026 19:21:31 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd9bc9c64dbbbe80cfab80ed3a5f6b6ba94f4f058b3146e076a1f4fbefe64da`  
		Last Modified: Thu, 26 Feb 2026 19:21:32 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88373b5b67d85768ba925199d76ebaa29900a50125be4a54a27ef1dec211f85e`  
		Last Modified: Thu, 26 Feb 2026 19:21:33 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95a59682c27dde2c6b6eb9668293e93e1330651fb612cc1defd971efdb48a42`  
		Last Modified: Thu, 26 Feb 2026 19:21:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbde451a1c11f9e3a0aa2bb95a44494f5179a9cc9a914f4bd322bfeb1d38a00`  
		Last Modified: Thu, 26 Feb 2026 19:21:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb33df5e865465db4591e3715c5c2d9acb5217f9c7e2b058020413c4682c3f07`  
		Last Modified: Thu, 26 Feb 2026 19:21:34 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02935c304ad2c96993aea7e1b33024c92f4711b4e0e3f22554a6e61996a00501`  
		Last Modified: Thu, 26 Feb 2026 19:21:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17f1ca3230cc3227642313a5fb1aabe0d7a7d55b6dbba645b7ba9a7f6e435ef`  
		Last Modified: Thu, 26 Feb 2026 19:21:36 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f38824a782c160d25a50913bdf543b497c5536e0d04b48fb3a82aa92571c58`  
		Last Modified: Thu, 26 Feb 2026 19:21:36 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef179f7533d71f31984d673861b584284a08637de3c7f1d2e53ecfa73a7dbdd`  
		Last Modified: Thu, 26 Feb 2026 19:21:37 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.1` - unknown; unknown

```console
$ docker pull kibana@sha256:32cb2f3526fba6b7b8077cdafa6d88ea49a8920051426b86cb0801c97abfe576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1768f656cc01e95f930f7582858d0bef9d603bef8470d30c0a8eb8fc32dc6bd0`

```dockerfile
```

-	Layers:
	-	`sha256:c721855c7df0401067c4c0ad553b89e4582fb88c3561ba55e130f4aed6a13875`  
		Last Modified: Thu, 26 Feb 2026 19:21:32 GMT  
		Size: 5.8 MB (5813717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be866cce58625e5f421af4bca187562197d5c08d3898a23acde27710a04e2860`  
		Last Modified: Thu, 26 Feb 2026 19:21:31 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4eb7ecb78e3177f60da3f3d878e9ce81f59e8c30ddb8e3f95d1411506ea05d0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.3 MB (465260513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f536d3fb24fcedc2141ba457f019ff396b4e4d8b51b6965de3f1d1ab1fdc04`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Thu, 26 Feb 2026 19:03:12 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Feb 2026 19:03:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 26 Feb 2026 19:19:40 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Feb 2026 19:19:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Feb 2026 19:19:40 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Feb 2026 19:19:41 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Feb 2026 19:19:41 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Feb 2026 19:19:41 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Feb 2026 19:19:41 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:19:41 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:19:41 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Feb 2026 19:19:41 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:19:42 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Feb 2026 19:19:43 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Feb 2026 19:19:43 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Feb 2026 19:19:43 GMT
LABEL org.label-schema.build-date=2026-02-24T03:42:25.053Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=342266a63c5cedf139febf5a982ceb9a1c46690b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-24T03:42:25.053Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=342266a63c5cedf139febf5a982ceb9a1c46690b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1
# Thu, 26 Feb 2026 19:19:43 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 26 Feb 2026 19:19:43 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 26 Feb 2026 19:19:43 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Feb 2026 19:19:43 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Feb 2026 19:19:43 GMT
USER 1000
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89ed966cac5c06e2f5a5f35323ba036508eea8728974b478f80693942dd4d3f`  
		Last Modified: Thu, 26 Feb 2026 19:20:49 GMT  
		Size: 19.5 MB (19475620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b795b61f1b4182b4898b8f0c060043d727c7ce6b9f5d6c0615dec4c11117a1d`  
		Last Modified: Thu, 26 Feb 2026 19:20:56 GMT  
		Size: 391.0 MB (391025473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ba23d58761ccc74a276a4dab48517b9c9dbde9d6b4f3a21801d027613b82b8`  
		Last Modified: Thu, 26 Feb 2026 19:20:48 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212fce94c032bf21a96583456a3edab49c78c4aa23a5111da452fafca56bc47`  
		Last Modified: Thu, 26 Feb 2026 19:20:49 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638d37396c6a54aa307829a58e8fff205fec4ad96c75f66f467db51235a51544`  
		Last Modified: Thu, 26 Feb 2026 19:20:49 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a19a7526d9932178b13fbcb3ef7bb21407a6f561ecfef2255fddeb6b2d90bd`  
		Last Modified: Thu, 26 Feb 2026 19:20:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1114b5eebd8fa3848175a9aef9deb1ce461ed3742c3951e2c41bbc629c6b0f`  
		Last Modified: Thu, 26 Feb 2026 19:20:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74579e9fd09dc0f84bb12b5b87604d9071ba0b763ac2baa451ecb7208bdc9fd4`  
		Last Modified: Thu, 26 Feb 2026 19:20:51 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b42c5ca665fe8155f99e10a69cb168a1055cbff134339f51b40abc2e7b24e0d`  
		Last Modified: Thu, 26 Feb 2026 19:20:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727c29fc50f8cbf9a3bc0103b119e51e08d63ab2a21b3b0aa5d817c47d7937bc`  
		Last Modified: Thu, 26 Feb 2026 19:20:52 GMT  
		Size: 73.4 KB (73447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec822b89a64db286d72cef180cf731d79eace642184cc0a6b2b7b615edef2fca`  
		Last Modified: Thu, 26 Feb 2026 19:20:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f1e82b5af3cb3bb30c7fd1fc4e43281e76c510a83ad83c827f24360dd23317`  
		Last Modified: Thu, 26 Feb 2026 19:20:53 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.1` - unknown; unknown

```console
$ docker pull kibana@sha256:a44193aedc2596b5e3e01f5dd43cdf5a8e4557c2c4600a1ec068efc5e5e6a9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f298f7cd664865188713d0792ab80f23c0d7f04b49afa4a96bddbcebd02a05c7`

```dockerfile
```

-	Layers:
	-	`sha256:16a309e9930fc03ee3de3fa45a8a5cb521e076aea68138622c1eac45467bd388`  
		Last Modified: Thu, 26 Feb 2026 19:20:48 GMT  
		Size: 5.8 MB (5812389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e650b49c53d8cedfa7ea05b3526a886b4a54042d8791d819614c10bad22b911`  
		Last Modified: Thu, 26 Feb 2026 19:20:48 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json
