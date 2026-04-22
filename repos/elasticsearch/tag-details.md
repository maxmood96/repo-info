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
$ docker pull elasticsearch@sha256:6ac3b64568aab22e7808fbe9359185e95948279e88eb86a0e2b9f09989878cc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:53729edc09018d29765ade50d28fdad442c0c6f84c675c40a824000a944d1fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738508561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e55b444b1d528f8189ebf3988ef9944c684aacac6819073580c763242850e46`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:17:42 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:42 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 22 Apr 2026 18:18:58 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:18:58 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:18:58 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Apr 2026 18:19:08 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:19:08 GMT
ENV SHELL=/bin/bash
# Wed, 22 Apr 2026 18:19:08 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 22 Apr 2026 18:19:08 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 22 Apr 2026 18:19:08 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 22 Apr 2026 18:19:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:19:08 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 18:19:08 GMT
CMD ["eswrapper"]
# Wed, 22 Apr 2026 18:19:08 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db45f40a6c781d7d088e0937b126f90a2e87f8ab340a73485a620b3684b58d15`  
		Last Modified: Wed, 22 Apr 2026 18:20:01 GMT  
		Size: 4.3 MB (4276366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae84b2cf58330696eb95f861392a66ad91c31b39d928980c0c7a7a0cc9173d8`  
		Last Modified: Wed, 22 Apr 2026 18:19:56 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f405c87f1dcd707ec61a7875a6428714f1a47471eca00207ba6af7ddf31a5308`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e897eee62fe7b9a805b8766312316a05f48d7145e5b5103f59a49be1eba30c`  
		Last Modified: Wed, 22 Apr 2026 18:20:15 GMT  
		Size: 694.1 MB (694117467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f02b9bf6eb9f64f7a4b9eee82053e45e2ed235ced04328dbc69bfbf81ae5dc`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34318704563d3ae649d3715211bf00c2f5d27bf85e839d0d47845af289de1478`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8dcfc0b7a0ddd892f4b91bc2af7443906efc676cfb7b04a189105b8eaa92f3`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 75.2 KB (75182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0b5356f53aaa2225e05855506f0a54a5b3225a01d43c760ec2a79c33440bfb`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:960819260bb0d6e2db78c913e295dc2035f87ae9a9a6c0aab32acbfd3b801652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5df823bbc94f7d9240ae153491d3812076be7be18c4f01990cbbf0045e75bef`

```dockerfile
```

-	Layers:
	-	`sha256:8f4a7b393b3773119ca0377bc339ab37603c729fd25d088991b08ea9c722254a`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 2.1 MB (2098165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c10a3d2dcbf0f5ea48b3d0c2ef7b794a4f4a267d756318e68fbea05983895ea`  
		Last Modified: Wed, 22 Apr 2026 18:20:00 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ada39bf6ffd4006f9ddafad13e78e7cb9011848230e9cc1c670e6bca4daa3ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582515655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557ae495c403b399e0ef48d25fd1da0c5078fc2c41cdc21c9c95b933f1a15eb8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:17:09 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 22 Apr 2026 18:18:09 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:18:09 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:18:09 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Apr 2026 18:18:16 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:18:16 GMT
ENV SHELL=/bin/bash
# Wed, 22 Apr 2026 18:18:16 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 22 Apr 2026 18:18:16 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 22 Apr 2026 18:18:16 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 22 Apr 2026 18:18:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:18:16 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 18:18:16 GMT
CMD ["eswrapper"]
# Wed, 22 Apr 2026 18:18:16 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e8788b95ae82b170d90d3a0f49acd8e344af859c7517019b20ec5b7cf41195`  
		Last Modified: Wed, 22 Apr 2026 18:18:57 GMT  
		Size: 4.3 MB (4284564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0e036a3b5ee68c7738d49c8ec2af4b3a68f8ca8f2bf8a47104913e1b46ca2c`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c89e860d32bef5a7824124ed114e512fc3352e503129dbf756abbdf52e54932`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70ec324e22df8de6cca5252ca593108057762fef2953fcd7ec6c2f8e97c6630`  
		Last Modified: Wed, 22 Apr 2026 18:19:12 GMT  
		Size: 539.9 MB (539938157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770d970e1768850a0940c0c932b81ab2cb612bf8936a1ba5ea9224f3f5c37c83`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f28f382ced9d2f6ed7b9bdad94f34326bbc3f58f3423ed41960d59721e1ba`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb4b2dbfad009f6b3a2bd651aae714feb38be5a67b186cdc8316cbf400ff24f`  
		Last Modified: Wed, 22 Apr 2026 18:18:58 GMT  
		Size: 74.1 KB (74108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad421c221b52a8a76351974bb39a258335a0302894528da90eda46675cf526a`  
		Last Modified: Wed, 22 Apr 2026 18:18:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0caead6a4788a86e30d9c6f5280a2708048794894b377941719e0888b5e9a125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df5df39b32ef67239636de4518427c9e06929d93d08c4dcdffa6309ada20e7`

```dockerfile
```

-	Layers:
	-	`sha256:a20d6493075a3a608e65017e43de86cbe3d4cea6d3b56fd94b99ce6c91037fea`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 2.1 MB (2098727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48ebab63fc320e3fcf2019e0fb09135886075f508788dc034ff859144061763`  
		Last Modified: Wed, 22 Apr 2026 18:18:56 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.3`

```console
$ docker pull elasticsearch@sha256:1d9ddbe28380c3305ef24c4364168030e4b8ce44834121f7c7dbdaedd2bb9cdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d06f5ef7ae191d03ccf78a37b01f087f89957b399dd4dc2d43003490b0c14edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716693133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d856dc19e0752836dfa45659fe95a2e6cc28bb1df7b5398652a9fbbbcb7b749`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:17:42 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:42 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 22 Apr 2026 18:18:54 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:18:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:18:54 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Apr 2026 18:19:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 22 Apr 2026 18:19:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 22 Apr 2026 18:19:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:19:04 GMT
ENV SHELL=/bin/bash
# Wed, 22 Apr 2026 18:19:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:19:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 22 Apr 2026 18:19:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 22 Apr 2026 18:19:04 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 22 Apr 2026 18:19:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 22 Apr 2026 18:19:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:19:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 18:19:04 GMT
CMD ["eswrapper"]
# Wed, 22 Apr 2026 18:19:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db228550e2d7d5bc1abf2c226220d3bfd75fe10ce37eab7da744462788bb5b99`  
		Last Modified: Wed, 22 Apr 2026 18:19:57 GMT  
		Size: 4.3 MB (4276357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae84b2cf58330696eb95f861392a66ad91c31b39d928980c0c7a7a0cc9173d8`  
		Last Modified: Wed, 22 Apr 2026 18:19:56 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b377be16daa7da95e271076bc87a7ff6fc3dca0a4728049cd86a3436b7e4f3`  
		Last Modified: Wed, 22 Apr 2026 18:19:57 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9a3a172ee592f0b3c261e650ac779d394512a3678334d5ffba833a7d686b6f`  
		Last Modified: Wed, 22 Apr 2026 18:20:24 GMT  
		Size: 672.3 MB (672302051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7061d39bda37c9d2995ad898a7d90528e84924f1d5607a98ad0c2ae39fac601a`  
		Last Modified: Wed, 22 Apr 2026 18:19:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddf8e652312d7c9470e08d450e2a507b5e3109ca8a8a024c8122560b729524c`  
		Last Modified: Wed, 22 Apr 2026 18:19:58 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae1f370f214e6686fd5f442f1921fe2bef6064f8ba16c789966bb0c9af0a81`  
		Last Modified: Wed, 22 Apr 2026 18:19:59 GMT  
		Size: 75.2 KB (75179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14061fd2d8339fbc9c709d0df73613065c11ed04977157dc6d643083abf918c8`  
		Last Modified: Wed, 22 Apr 2026 18:19:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:99e863bc7bf8b893c4918489f7181962b1eae4613967e2478550719d8808a2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbbc78d24f72e0ce703b15274e759c55384bdd556e0f640cbe0773628b40ab2`

```dockerfile
```

-	Layers:
	-	`sha256:579f1159114e1f0cf3f2805b972bba9a19dec7b9608def1f82c0e6dffe5aaf06`  
		Last Modified: Wed, 22 Apr 2026 18:19:56 GMT  
		Size: 2.1 MB (2089805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6186da0bd84e44087745044cc84d7c10fdd1417f73ef3696b0035d508fb838ba`  
		Last Modified: Wed, 22 Apr 2026 18:19:56 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ee86295db178770c665359ac82377261f8219d34264068cc2b2c34ead3b3d2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560693492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd99198d4430c8f894055f73510b0950d32fa3c56b619e3383a730962722ec55`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:17:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:17:11 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Wed, 22 Apr 2026 18:17:29 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:17:29 GMT
COPY /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:17:29 GMT
WORKDIR /usr/share/elasticsearch
# Wed, 22 Apr 2026 18:17:36 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Wed, 22 Apr 2026 18:17:36 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Wed, 22 Apr 2026 18:17:36 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:17:36 GMT
ENV SHELL=/bin/bash
# Wed, 22 Apr 2026 18:17:36 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:17:36 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Wed, 22 Apr 2026 18:17:36 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Wed, 22 Apr 2026 18:17:36 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 22 Apr 2026 18:17:36 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Wed, 22 Apr 2026 18:17:36 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:17:36 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 18:17:36 GMT
CMD ["eswrapper"]
# Wed, 22 Apr 2026 18:17:36 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92487dfce1760cf92b0319e149bc576df153bf25d6c6102a410ea548bdc4ea58`  
		Last Modified: Wed, 22 Apr 2026 18:18:15 GMT  
		Size: 4.3 MB (4284546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e53334c4cccf8d0a68aa522bd6fd5e0e37c5912cfed64c84428265d96283e46`  
		Last Modified: Wed, 22 Apr 2026 18:18:15 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6814d4738125298bd4314313b2b1e7d4b3bfe5eb79a5980a15a533362da00`  
		Last Modified: Wed, 22 Apr 2026 18:18:15 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f8f78cc7907f438c049ec394a0287dee3e850e9264daae0652d95475cb9c0`  
		Last Modified: Wed, 22 Apr 2026 18:18:26 GMT  
		Size: 518.1 MB (518116009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281cf59af17d495ebc4a6cd132bb937fe33ef9429316d080edcc03fa6027de11`  
		Last Modified: Wed, 22 Apr 2026 18:18:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862a22c474281a4e89b3f35aa36cfdbbc9e4b1a8d4bd180deed9b98907e7fe9f`  
		Last Modified: Wed, 22 Apr 2026 18:18:16 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8f637964a338ff8bec754bca71a271e268bb1e03317b47f0a2c8971adf9f98`  
		Last Modified: Wed, 22 Apr 2026 18:18:17 GMT  
		Size: 74.1 KB (74107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c0e615883c150d697938348f48625244a9cc46fca9d15f690d86bba6492ea`  
		Last Modified: Wed, 22 Apr 2026 18:18:17 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f1944de775593d59c45b5b1143808f553cf1bbe72c6f7ce4e68234968a3e85f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b7fae6d0a871486117ec4fc00ab30238f4e4aa49cb054704d445a1c3b8ec87`

```dockerfile
```

-	Layers:
	-	`sha256:42f600057340ae129bc3aaff2daa3da472677b600527674b5b445102ab058f15`  
		Last Modified: Wed, 22 Apr 2026 18:18:15 GMT  
		Size: 2.1 MB (2090367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:763785cc1f3cb8304269e9f50bb465c9b7d79524652a60985483c9ce0c8da71e`  
		Last Modified: Wed, 22 Apr 2026 18:18:15 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
