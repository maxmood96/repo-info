<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.12`](#kibana81912)
-	[`kibana:9.2.6`](#kibana926)
-	[`kibana:9.3.1`](#kibana931)

## `kibana:8.19.12`

```console
$ docker pull kibana@sha256:72ac4cc9338c720f6e237f405e14ac1598b8286405a70325b0431d4cda770ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.12` - linux; amd64

```console
$ docker pull kibana@sha256:8d97071593a6791cd6a11662010e384bcb6daa0dbf1165f590f2c117c6ea730a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442064411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8f972c65a064bc0aec8d89c911e65eac0c0c260282a10f80ca8288fd49b50b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 17 Mar 2026 01:39:34 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:48:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 17 Mar 2026 01:48:52 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Mar 2026 01:48:52 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 17 Mar 2026 01:48:53 GMT
RUN fc-cache -v # buildkit
# Tue, 17 Mar 2026 01:48:53 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Mar 2026 01:48:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 17 Mar 2026 01:48:53 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Mar 2026 01:48:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:48:53 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 17 Mar 2026 01:48:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:48:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 17 Mar 2026 01:48:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 17 Mar 2026 01:48:55 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 17 Mar 2026 01:48:55 GMT
LABEL org.label-schema.build-date=2026-02-24T03:15:27.497Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a2a93735478172a315d2ced4aded3024cc029648 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-24T03:15:27.497Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a2a93735478172a315d2ced4aded3024cc029648 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Tue, 17 Mar 2026 01:48:55 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 17 Mar 2026 01:48:55 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 17 Mar 2026 01:48:55 GMT
USER 1000
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f12b00a496c50eb6793e9f6cfe419a20246ce2f75dbb558a2cdf5c0a646976d`  
		Last Modified: Tue, 17 Mar 2026 01:49:56 GMT  
		Size: 9.4 MB (9434320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f164f437c9e79a892e33aa2ce9bb4bf8ff57281bc7fca9f190d347b596d3092`  
		Last Modified: Tue, 17 Mar 2026 01:50:03 GMT  
		Size: 386.3 MB (386254362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de72180d34e063990bfbafbaec4cdb22669a6d1fcf70481a8ebc62ba5c24bafc`  
		Last Modified: Tue, 17 Mar 2026 01:49:55 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b395e4deb91d48b22fd9fd5cf87ddd266b7521f15d0c4cd23184832d7430772`  
		Last Modified: Tue, 17 Mar 2026 01:49:56 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80cafa3c3d3b7cc09177a1cfe2e25202ca2983643aeca8674d8d2b96d81aa6ee`  
		Last Modified: Tue, 17 Mar 2026 01:49:56 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4135d0a2c1ce9701b397a0974dbad6a0663e7685c140c48e739f331bcbddc45`  
		Last Modified: Tue, 17 Mar 2026 01:49:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2715ae9e8e3cb9f98128474d01e5af303514e194852589a76d8aa75a59b5bf1a`  
		Last Modified: Tue, 17 Mar 2026 01:49:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c29c76df05cbbcbbe8d5300709fcfcbb39811e16476bcc03a698646497fb61`  
		Last Modified: Tue, 17 Mar 2026 01:49:58 GMT  
		Size: 4.8 KB (4818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6249a6fd745c474385bc5fbb86dad8e560cc03e795f22f5f5a9b5fea548967c`  
		Last Modified: Tue, 17 Mar 2026 01:49:58 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7527c0b68f6a2c825e00f254383ea86a39da1c99501ef05f00e98b68a859ee7`  
		Last Modified: Tue, 17 Mar 2026 01:49:59 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfda4e1e56730443f9bf91f3ea0e61331266801abc3aa27856a921daa46793`  
		Last Modified: Tue, 17 Mar 2026 01:49:59 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.12` - unknown; unknown

```console
$ docker pull kibana@sha256:0fbb8ee748d26bb2e3c01d58521f2f54c725ffe37a9ce7f13e607fa99ee842d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca8486c7d2cbe41a4b1eb68e9c93d9aafd1e1b555be53c147fbbb90d0a721cd`

```dockerfile
```

-	Layers:
	-	`sha256:004d579d0252c4d30b69f972b5647b6237b78afcaac5f9cc9c2e7baa68399856`  
		Last Modified: Tue, 17 Mar 2026 01:49:55 GMT  
		Size: 4.9 MB (4922007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8564a972ad252b51b72904f3b5f4f28afee0d0ba9765a87c4f3b56c54f6af00b`  
		Last Modified: Tue, 17 Mar 2026 01:49:55 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.12` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:46820fdcc7113a727c423769276d27156444a74388545b335c8ae460b0eb07ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.0 MB (454968819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7f397529a6ca0f639b3eb1aced2238dee310d28409c445d74d0bdf9a69fc14`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:56 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 17 Mar 2026 01:40:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:48:28 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 17 Mar 2026 01:48:28 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Mar 2026 01:48:28 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 17 Mar 2026 01:48:29 GMT
RUN fc-cache -v # buildkit
# Tue, 17 Mar 2026 01:48:29 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Mar 2026 01:48:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 17 Mar 2026 01:48:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Mar 2026 01:48:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:48:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 17 Mar 2026 01:48:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:48:30 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 17 Mar 2026 01:48:31 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 17 Mar 2026 01:48:31 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 17 Mar 2026 01:48:31 GMT
LABEL org.label-schema.build-date=2026-02-24T03:15:27.497Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a2a93735478172a315d2ced4aded3024cc029648 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.12 org.opencontainers.image.created=2026-02-24T03:15:27.497Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a2a93735478172a315d2ced4aded3024cc029648 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.12
# Tue, 17 Mar 2026 01:48:31 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 17 Mar 2026 01:48:31 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 17 Mar 2026 01:48:31 GMT
USER 1000
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8a19a91b90a684139bc594bf98ed7f0ef74d4386a18fde48194510cae81e96`  
		Last Modified: Tue, 17 Mar 2026 01:49:37 GMT  
		Size: 9.5 MB (9451906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ad60d7ae2cec1e3f55399371c3d531cfcb6bcda7167cab9e3543f6bf6a5e4e`  
		Last Modified: Tue, 17 Mar 2026 01:49:44 GMT  
		Size: 400.0 MB (400007383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee998fd3551aa31ada9a47eeba6d086ba4bc07fd9ef5f3549af91e51162e15`  
		Last Modified: Tue, 17 Mar 2026 01:49:36 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a2f6b95cd872dc2896613c47a3669a41a23491a1bb9dc1910b5c99e85ccff3`  
		Last Modified: Tue, 17 Mar 2026 01:49:37 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488985737813ea1821233d91fa823de0f8d32803328fc2a1ae8f8b83a66d5ee4`  
		Last Modified: Tue, 17 Mar 2026 01:49:37 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e43fe072e7bffac62f933bdd5be2e224ad8a2b972f01e6a8c3d7276619ac63`  
		Last Modified: Tue, 17 Mar 2026 01:49:38 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff6c91d9cd858bfd6c12f5470da857974f0f3b599c9eb30115bff1e328d863`  
		Last Modified: Tue, 17 Mar 2026 01:49:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf5ead781887272fa6a0e9b29080ec7bb7822dbb393d4fd80f3dea4865617b1`  
		Last Modified: Tue, 17 Mar 2026 01:49:39 GMT  
		Size: 4.8 KB (4823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2f6cd4b7155e3cf4b8e82c1bb8f9f43defef563e170664649d1605bd570370`  
		Last Modified: Tue, 17 Mar 2026 01:49:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e236ae4f653ab59fdbf8eff95a068fd1f2283dbdbb9d76ebd6bffd743361640`  
		Last Modified: Tue, 17 Mar 2026 01:49:40 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185e8a62d633c5a6fb167eba1ce122189ba36cac4fe35916e41d9b97a010f4e3`  
		Last Modified: Tue, 17 Mar 2026 01:49:40 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.12` - unknown; unknown

```console
$ docker pull kibana@sha256:82616c67f379513682aed37e75c08e84d1338ad32d548956b8af6d73d2e5faa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4964234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8b2dec08d6c95d31d3ee80269a4505e61fd262e9bce8051b48d0a85da346bd`

```dockerfile
```

-	Layers:
	-	`sha256:a21532ebf4b6cbf65b660c45189ec15d34d48a105356ca104f8e3eb15bc3019e`  
		Last Modified: Tue, 17 Mar 2026 01:49:36 GMT  
		Size: 4.9 MB (4923071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2906bb6966d231689418ccf17db41fb0a11f80eb0e212c7fd29bf11418a10d20`  
		Last Modified: Tue, 17 Mar 2026 01:49:36 GMT  
		Size: 41.2 KB (41163 bytes)  
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
