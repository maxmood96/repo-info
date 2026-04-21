<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.19.14`](#elasticsearch81914)
-	[`elasticsearch:9.2.8`](#elasticsearch928)
-	[`elasticsearch:9.3.3`](#elasticsearch933)

## `elasticsearch:8.19.14`

```console
$ docker pull elasticsearch@sha256:33a80e56d13fb6773b92f86f87736b4bde158d4b8f26a6c831db578ce39fc526
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.14` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6e7f9b9392e465c39d270787acbc426430f3b956584312f1d0e2883edb9ad6bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **714.8 MB (714781022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbd36c9aceedbed48c8902af8d4ee5a48915221e2c30f52d0b38859df444004`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Wed, 15 Apr 2026 20:35:32 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 15 Apr 2026 20:35:33 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 15 Apr 2026 20:35:33 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Apr 2026 20:35:33 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 15 Apr 2026 20:36:46 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:36:46 GMT
ENV SHELL=/bin/bash
# Wed, 15 Apr 2026 20:36:46 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 15 Apr 2026 20:36:46 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 15 Apr 2026 20:36:46 GMT
LABEL org.label-schema.build-date=2026-04-02T15:09:12.561504739Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f9adf4c29021dbda28cae7d9c11924471798723d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T15:09:12.561504739Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f9adf4c29021dbda28cae7d9c11924471798723d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 15 Apr 2026 20:36:46 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:36:46 GMT
CMD ["eswrapper"]
# Wed, 15 Apr 2026 20:36:46 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a66118f70c8a2306ffbc4c696c8e748b6134f4d92cea02abdb4a65274e37bc`  
		Last Modified: Wed, 15 Apr 2026 20:37:40 GMT  
		Size: 4.5 MB (4496384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224cd9cf6cf6d9ea7b81ce0310cb96d33249abbccbc613af9200471a7550be5`  
		Last Modified: Wed, 15 Apr 2026 20:37:39 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd01248626a3dc5f3a92bba7595b0b496ad81c915331dfe7215d7a38a3da44a`  
		Last Modified: Wed, 15 Apr 2026 20:37:54 GMT  
		Size: 680.3 MB (680256726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e141b4ea29b318a3c1d6f4348e864bda3c39893d6716c0376b64b318e602c4cf`  
		Last Modified: Wed, 15 Apr 2026 20:37:40 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a13b2493950ca976147332e930f3c17b649e6d7b81ca6186821c134e02731d`  
		Last Modified: Wed, 15 Apr 2026 20:37:41 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c31b7a1d2bb585c39c90965454db46f20a94929dd2a5e1c179d5a4a27118f`  
		Last Modified: Wed, 15 Apr 2026 20:37:41 GMT  
		Size: 164.2 KB (164191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b054cf1d8f78025379fe11a9f09c8458b827fd4bc76ae893cce81e536e1b7c54`  
		Last Modified: Wed, 15 Apr 2026 20:37:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bc1b5716e7cc57c68ca13c1083ad705cc4947d4e0bbbe9237c2871e8f94986`  
		Last Modified: Wed, 15 Apr 2026 20:37:42 GMT  
		Size: 115.5 KB (115528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.14` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fba74613270899a9b27a5f8ce43f47af627bce08260ffd8c3ce7d0a9faf0decc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2afa49a41b51d4da79c0fb3a0cbbd3d68abc165c18e55bba8e70a81c910c926`

```dockerfile
```

-	Layers:
	-	`sha256:db494b5250bb6ebd9333202952081a2f29fe79205f4db1be73b5c8d02299c15d`  
		Last Modified: Wed, 15 Apr 2026 20:37:40 GMT  
		Size: 3.2 MB (3208984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42f59d9682d0fa9259b397e3d43b10316143590fe17a8a7c4345733dc677fb4a`  
		Last Modified: Wed, 15 Apr 2026 20:37:40 GMT  
		Size: 36.8 KB (36816 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.14` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:2fa325e042cfe8933306ee228338c804318cde6f923df4305b54016e402695ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.7 MB (562662545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461bfcea521600b4e16fdae91950b6f958c66b75e4f3e27dd1228ce39ccb75cf`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Wed, 15 Apr 2026 20:35:40 GMT
RUN ln -sf bash /bin/sh && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Wed, 15 Apr 2026 20:35:40 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home --shell /bin/bash elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 15 Apr 2026 20:35:40 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Apr 2026 20:35:40 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 15 Apr 2026 20:36:48 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Wed, 15 Apr 2026 20:36:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 15 Apr 2026 20:36:48 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:36:48 GMT
ENV SHELL=/bin/bash
# Wed, 15 Apr 2026 20:36:49 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:36:49 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 15 Apr 2026 20:36:49 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 15 Apr 2026 20:36:49 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Wed, 15 Apr 2026 20:36:49 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 15 Apr 2026 20:36:49 GMT
LABEL org.label-schema.build-date=2026-04-02T15:09:12.561504739Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f9adf4c29021dbda28cae7d9c11924471798723d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T15:09:12.561504739Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f9adf4c29021dbda28cae7d9c11924471798723d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 15 Apr 2026 20:36:49 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:36:49 GMT
CMD ["eswrapper"]
# Wed, 15 Apr 2026 20:36:49 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b2411dfd162c3bf0ded762fc11c5ff5273b285b1bca83258791d20287f9d2`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 4.5 MB (4502660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cff13d76b57418cd747ef4ee73acb32a6b2c9275f1767a6e8089017fb1ff1e6`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16866d546481584ddfe103a5022b773ec36be0ad90b2bb21f4df4f8928994b9`  
		Last Modified: Wed, 15 Apr 2026 20:37:41 GMT  
		Size: 529.0 MB (528993089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807ebc3ab322d6aeddd7ddb6ad7aabe810b9ec4eec19c897949bb91a768341a5`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae507c24c34488c8f849723ac4c167a06ed53615fcf51309443417f645ecfeb4`  
		Last Modified: Wed, 15 Apr 2026 20:37:28 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf6c173f2623e1b38af5853b4f85bc0566fcb19138c3940d54174ea590c75b1`  
		Last Modified: Wed, 15 Apr 2026 20:37:28 GMT  
		Size: 160.7 KB (160695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f3b21d5a534c687e5a8d234a7a1e8b01fcb81bff5b7f991b29c54192b9bd7`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71388983d29cfa138ded3a8bbdb9f2fa795288e10a7c497269e097ff55af0162`  
		Last Modified: Wed, 15 Apr 2026 20:37:29 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.14` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6c086307c021561e5fccbed7c5592db0fe7e9a262dd69a344aad507d5839f948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8fe1a9b3a1b8641f17dcc3c0eb0dfa3ca44b7dd967b488018b6b12798c0dbb`

```dockerfile
```

-	Layers:
	-	`sha256:c296c97ce4cad72b574f5a9a2f3d32bbd47d88fe4c2ecc52c611191dad22b077`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 3.2 MB (3209397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d33bd74c8f4508a83e354d7afa6437b269e90e764f80f27e1cfed82c7626b056`  
		Last Modified: Wed, 15 Apr 2026 20:37:27 GMT  
		Size: 37.0 KB (37019 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.2.8`

```console
$ docker pull elasticsearch@sha256:fb3e46faf94a6463bffa5e66cd768055b76dfe0234acccdc33c92a62f27aa097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e1bb27939b8ef87d56cc2ba142c03d6b87536a60f36d26946efcb3b998bb01ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738501123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9db2607c7dfa247a282f1db0985be5a3b0e58fd9090eab9f0e5ebc3eb36ebfb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:47:05 GMT
ENV container oci
# Mon, 20 Apr 2026 00:47:06 GMT
COPY dir:95d17c57ef40a5dba79704e92b9c5527d3acb3226364e42c0d41763471e61ce6 in /      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:47:06 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:46:48Z" "org.opencontainers.image.created"="2026-04-20T00:46:48Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:46:48Z
# Mon, 20 Apr 2026 23:06:56 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 20 Apr 2026 23:08:08 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:08:08 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:08:08 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 20 Apr 2026 23:08:18 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 20 Apr 2026 23:08:18 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 20 Apr 2026 23:08:18 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:08:18 GMT
ENV SHELL=/bin/bash
# Mon, 20 Apr 2026 23:08:18 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:08:18 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 20 Apr 2026 23:08:18 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 20 Apr 2026 23:08:18 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Mon, 20 Apr 2026 23:08:18 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 20 Apr 2026 23:08:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:08:18 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:08:18 GMT
CMD ["eswrapper"]
# Mon, 20 Apr 2026 23:08:18 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7e3fbd5e4ab180e0609e5563bc2f414fcab5c08ec4063f1424469e61ceaf41`  
		Last Modified: Mon, 20 Apr 2026 23:09:11 GMT  
		Size: 4.3 MB (4277521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671eb0375ccc779a4fcf1180b51a551ad9c4600fdaaf7faa908ec5862a74dc57`  
		Last Modified: Mon, 20 Apr 2026 23:09:10 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5b57c28d941186f720b585b685528d9c3fb8e906836d7a1ab9ffefcbb6f216`  
		Last Modified: Mon, 20 Apr 2026 23:09:11 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453f8096d8ee95a9bfd48c70a5d4ab5b08abc719fa7fa5816b3604efd6691de4`  
		Last Modified: Mon, 20 Apr 2026 23:09:25 GMT  
		Size: 694.1 MB (694117355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc54a15ba2d2b7a5bd96e9ad644ea436deb8972a3686a9fe3beae114516b63`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a872102fdf870b033cf902b5caa26064b406a8d3a80c45011e3d203d045db32`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac67007f8aacb5ff6b8e3664d973fecffd9372c20af56aa7af849f084af66d9`  
		Last Modified: Mon, 20 Apr 2026 23:09:12 GMT  
		Size: 75.2 KB (75181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc10b5f2e231bdf0e35c0ef9825799519624343b1f0f9f2cb364793faacd138`  
		Last Modified: Mon, 20 Apr 2026 23:09:13 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:cd43c592812d20df8a399ee71b7b7c3e13f2e415ff303f9d122cbde7f010c93c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b09de86e1023403b35ac3370cb264f31d008f536af8cabdd459a1db64362c6e`

```dockerfile
```

-	Layers:
	-	`sha256:8e6b59815e84329240d51dc38f7df3cf206331394497bd8d5d560b806f89bbc7`  
		Last Modified: Mon, 20 Apr 2026 23:09:11 GMT  
		Size: 2.1 MB (2098165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b2f1b790d3bdd377ebb88a15369fe9007e800e8262f50e1c59db9c130d96a3`  
		Last Modified: Mon, 20 Apr 2026 23:09:11 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a648b76c730a854331806ca4cfa0405ad5ea15352f6a61a1bbf1a8e98ffca8fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582512301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296d4afcb6898d420c92f2716855322cecbc1657b7d8a47ccfcbd262c6b48565`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:49:28 GMT
ENV container oci
# Mon, 20 Apr 2026 00:49:29 GMT
COPY dir:2db86b8c6d033296a751d728266ea755c08c1579f6b374a8f32773f7c153c4a3 in /      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:49:29 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:49:15Z" "org.opencontainers.image.created"="2026-04-20T00:49:15Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:49:15Z
# Mon, 20 Apr 2026 23:04:39 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:39 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 20 Apr 2026 23:05:35 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:05:35 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:05:35 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 20 Apr 2026 23:05:41 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 20 Apr 2026 23:05:41 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 20 Apr 2026 23:05:41 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:05:41 GMT
ENV SHELL=/bin/bash
# Mon, 20 Apr 2026 23:05:41 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:05:41 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 20 Apr 2026 23:05:41 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 20 Apr 2026 23:05:41 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Mon, 20 Apr 2026 23:05:41 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 20 Apr 2026 23:05:41 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:05:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:05:41 GMT
CMD ["eswrapper"]
# Mon, 20 Apr 2026 23:05:41 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc6a446e4cf51b996316416f4c527db40f26ff8f92c2fbe85aec217524f1651`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 4.3 MB (4285561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d279963251bc5d1be64b30006131cacbbb27394becc8bc7d93b4af71ce0b5e53`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c424c2f6689a1e75210e287b4d4d10eaa9abd41c541a3c2d3e8d4e81cd00e19c`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbc830100e682adbe68c02d79c19559a3dd5aa19fd4292ee446e824ecba91a7`  
		Last Modified: Mon, 20 Apr 2026 23:06:33 GMT  
		Size: 539.9 MB (539938172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2f51f4be2e8c067b28a94fbcd13a8579b1f253dc3567ec77ca6ca318265e4f`  
		Last Modified: Mon, 20 Apr 2026 23:06:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6ae2892e38250cb21684b164a8f5858d85c611b6e038e81dc9cf44122b58d5`  
		Last Modified: Mon, 20 Apr 2026 23:06:22 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424f02c8c9db679bd42517717ad0e4eaebe6f2a836a08f3f5d0f1e1fe60db698`  
		Last Modified: Mon, 20 Apr 2026 23:06:23 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0c2f2dffccb9f9faf598fb16217ff9cdc09c7c68f861fff28e9357ea25aeba`  
		Last Modified: Mon, 20 Apr 2026 23:06:24 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f3cf5d67b7b71da8fa7349a878c7219387f3bad4efc44704c1a21b65e13ac971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0645fd4865af87cff061b2318075d45c96a08b3d4be47acb20e05139e0ccc52`

```dockerfile
```

-	Layers:
	-	`sha256:cd86bf26f5649b0c8f5422a754ca4295d550516ebc7dcbab85d9b80dfa51252f`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 2.1 MB (2098727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ca21c9e02658df7dd7e404cc904aa1cc58c34e1585865ab966dc36b75724e9`  
		Last Modified: Mon, 20 Apr 2026 23:06:21 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.3`

```console
$ docker pull elasticsearch@sha256:2f3054e283b5fc121cb011fc2423fdb737ba72e8af6e88619c7aebf637ed792c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a469f4288bf76b9640fc054f8fd74f7f2aeffc501916633161c3aff36fee15a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716685696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435df95acccf448b6d65eb4e8f1dc56bf867073204e38da440135c8faff9f8db`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:47:05 GMT
ENV container oci
# Mon, 20 Apr 2026 00:47:06 GMT
COPY dir:95d17c57ef40a5dba79704e92b9c5527d3acb3226364e42c0d41763471e61ce6 in /      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:47:06 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:46:48Z" "org.opencontainers.image.created"="2026-04-20T00:46:48Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:46:48Z
# Mon, 20 Apr 2026 23:06:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:58 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 20 Apr 2026 23:08:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:08:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:08:04 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 20 Apr 2026 23:08:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 20 Apr 2026 23:08:13 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 20 Apr 2026 23:08:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:08:13 GMT
ENV SHELL=/bin/bash
# Mon, 20 Apr 2026 23:08:13 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:08:13 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 20 Apr 2026 23:08:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 20 Apr 2026 23:08:13 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Mon, 20 Apr 2026 23:08:13 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 20 Apr 2026 23:08:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:08:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:08:14 GMT
CMD ["eswrapper"]
# Mon, 20 Apr 2026 23:08:14 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da108d7d2cb49b3eb80802e3c9a1292778883f83c423bc6a0ad4d86b1a11c9ef`  
		Last Modified: Mon, 20 Apr 2026 23:09:04 GMT  
		Size: 4.3 MB (4277504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de8394f10aaf2c264b10a7b5257479a4e9ded1b9a4beaec6e9b4fd5e68c3828`  
		Last Modified: Mon, 20 Apr 2026 23:09:03 GMT  
		Size: 1.5 KB (1537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe371f7b84eb087d2fe8342761cb5136d0a9af95c0d753b21b574a9eb7280ac`  
		Last Modified: Mon, 20 Apr 2026 23:09:03 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18ccd248edccc4c059f829c15dfcf5d42e7b3c342aeba49d77d292cea0ccf25`  
		Last Modified: Mon, 20 Apr 2026 23:09:17 GMT  
		Size: 672.3 MB (672301938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68490aba05384f5424777d38ed1d00e402695c73b5ac33fbb8d0854a92f40aaa`  
		Last Modified: Mon, 20 Apr 2026 23:09:05 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b5dcc552242af22f7010ba96f7003f2f0db70074b0081c448ce17243654e80`  
		Last Modified: Mon, 20 Apr 2026 23:09:05 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdb63bd6b5978382188d3743d64c19d0f99d7e81f9b8d0e82669f35c5a88408`  
		Last Modified: Mon, 20 Apr 2026 23:09:05 GMT  
		Size: 75.2 KB (75177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f195b4e00dffb3f7ee3916fe8995d933af6753e65cea95363f317cd1deeab`  
		Last Modified: Mon, 20 Apr 2026 23:09:06 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:d389152e85c0f639e1003bf1ec54c883f65ab935066615f1c5b0c3761bbfb4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b460d7c37b446e270bf87d2ef6792fa31566db767bd95a2119c08e621fc6a5c1`

```dockerfile
```

-	Layers:
	-	`sha256:670810cf7202752235acd31c1e2e054b578e8ad0718734474b893d5083aa6133`  
		Last Modified: Mon, 20 Apr 2026 23:09:04 GMT  
		Size: 2.1 MB (2089805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a042569c68c186ff1e67fc2117f40efbbf98268186beb2674a5394cdfa1e1cf`  
		Last Modified: Mon, 20 Apr 2026 23:09:03 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:147deac26f63909bce1d11ec19a07f7424d587522f61d6ac0d07c22df5c6d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560690129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daf810954f741c07d69f797230da6dce31d0ab56fda979faae718de5ecdc4bb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:49:28 GMT
ENV container oci
# Mon, 20 Apr 2026 00:49:29 GMT
COPY dir:2db86b8c6d033296a751d728266ea755c08c1579f6b374a8f32773f7c153c4a3 in /      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:49:29 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:49:15Z" "org.opencontainers.image.created"="2026-04-20T00:49:15Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:49:15Z
# Mon, 20 Apr 2026 23:04:35 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:35 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 20 Apr 2026 23:05:29 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:05:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:05:29 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 20 Apr 2026 23:05:36 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 20 Apr 2026 23:05:36 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 20 Apr 2026 23:05:36 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:05:36 GMT
ENV SHELL=/bin/bash
# Mon, 20 Apr 2026 23:05:36 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:05:36 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 20 Apr 2026 23:05:36 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 20 Apr 2026 23:05:36 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Mon, 20 Apr 2026 23:05:36 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 20 Apr 2026 23:05:36 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:05:36 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 20 Apr 2026 23:05:36 GMT
CMD ["eswrapper"]
# Mon, 20 Apr 2026 23:05:36 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b73a43afd62b390ff380229b1816601c036beceb077adcebfd4e30fc98f3692`  
		Last Modified: Mon, 20 Apr 2026 23:06:14 GMT  
		Size: 4.3 MB (4285445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbdeec2d08ad0196d5df2adcc08242e19c37ca413f2eab3f96d6788572011b0`  
		Last Modified: Mon, 20 Apr 2026 23:06:14 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0d2d639ff1b4d4a68e8953155e229731c5322f856a2bbb3fe99c92a4b4094a`  
		Last Modified: Mon, 20 Apr 2026 23:06:14 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41021a10e4c18dfba138bd0afffc638ed2cf22fc304abc1b308208059612efda`  
		Last Modified: Mon, 20 Apr 2026 23:06:24 GMT  
		Size: 518.1 MB (518116119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e979a7df2a953499b4cbf40046f304e0143821ddf261d990075c81b2720359`  
		Last Modified: Mon, 20 Apr 2026 23:06:15 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d433192e14aa25a68efa2da765e664317b53b80462d16024fc310cff2694d990`  
		Last Modified: Mon, 20 Apr 2026 23:06:15 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0ea316e123e4d26b815e25e612c154d7d61e3ca95f8a87a23da36ea2246fd3`  
		Last Modified: Mon, 20 Apr 2026 23:06:16 GMT  
		Size: 74.1 KB (74105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cad4615659f30f8e2a05105ad16018ea94fb0ecd3ebc4d0dc677b32204babd8`  
		Last Modified: Mon, 20 Apr 2026 23:06:16 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:79d2393995b7f6f2558e84c634e58c552ee1f81a3df1d7cd4b57d67088894787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370ec2235044eb700f99e4716c835e9fc89490406cdaccaeecf4f26898120a51`

```dockerfile
```

-	Layers:
	-	`sha256:695ffadcfad192f8d3a9211ad61f08537b30bea5238c2cf4137916b95eb98aeb`  
		Last Modified: Mon, 20 Apr 2026 23:06:14 GMT  
		Size: 2.1 MB (2090367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61141df4bda07f3382b0d5d353d6d69703f877a84b788f7771653a3ccc47d9bd`  
		Last Modified: Mon, 20 Apr 2026 23:06:14 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
