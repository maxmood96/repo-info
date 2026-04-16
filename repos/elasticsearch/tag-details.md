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
$ docker pull elasticsearch@sha256:8f9a491d2daa880935dfc1c6461c51faeef090a7b788be668fead994f63aff31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.2.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:a9493965f9de5633da76f36b07ebcf290e0034a44480e7169a0efb3427ef8977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **738.5 MB (738501555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56ef10f2339219d1fbe270e2077104b3b13196ff985d15263f3f142fd69a59`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:46:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:46:08 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:47 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 14 Apr 2026 20:46:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 14 Apr 2026 20:46:57 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 14 Apr 2026 20:46:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:57 GMT
ENV SHELL=/bin/bash
# Tue, 14 Apr 2026 20:46:57 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:46:57 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 14 Apr 2026 20:46:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 14 Apr 2026 20:46:57 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Tue, 14 Apr 2026 20:46:57 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 14 Apr 2026 20:46:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:46:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 20:46:57 GMT
CMD ["eswrapper"]
# Tue, 14 Apr 2026 20:46:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920f9a8d2993bd38edcb0f2433f5be618d4e5f0772a5f820e3980ecb21542ad`  
		Last Modified: Tue, 14 Apr 2026 20:47:51 GMT  
		Size: 4.3 MB (4277532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998da302dd72b2ea1561fe360d6ccd23cce9484c8b6c22f819bd0a41d0d6563b`  
		Last Modified: Tue, 14 Apr 2026 20:47:50 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b9bc962ceb8c0cd1d7979084a51905bef29c4b1c65d24deb2efd81e9946892`  
		Last Modified: Tue, 14 Apr 2026 20:47:50 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe03f68774d9a0ddecda8a5da64746e17bca42b948926969cab13442fe6a3bf`  
		Last Modified: Tue, 14 Apr 2026 20:48:07 GMT  
		Size: 694.1 MB (694117512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70f5b31e18b816756925bf13ad401cef5fdcaf3c613e9067a2e9ace5c80f7b`  
		Last Modified: Tue, 14 Apr 2026 20:47:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895725aeb3507146542b59322b60ed7d039fb2d6e0b1edad019e7c9db9d255e4`  
		Last Modified: Tue, 14 Apr 2026 20:47:52 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b960c3cf6cff85eb78de5a80cee67f2f23888af7234e9c34819b60caf4db15`  
		Last Modified: Tue, 14 Apr 2026 20:47:52 GMT  
		Size: 75.2 KB (75178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab58605a64fe44db5d20b333e96790893388932e76f2b8397a385b72a3a9a91d`  
		Last Modified: Tue, 14 Apr 2026 20:47:53 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6b89f148e72c26a88344049227d8d4177908c4fce27d6a35e9cd3bc816460ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833141adc3933bdb62014fd0fd5338bccca1f07a6c25dd4ea27c9c71bc222f4e`

```dockerfile
```

-	Layers:
	-	`sha256:745d3cfe44d8f440fbf52de949dac958fe7d3a42d13b25cc23713305eeb375d3`  
		Last Modified: Tue, 14 Apr 2026 20:47:50 GMT  
		Size: 2.1 MB (2098165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc35307884b38adb7be8137899004a47b03e9205ad1dd7f2235b14d6e6b8e95`  
		Last Modified: Tue, 14 Apr 2026 20:47:50 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.2.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c51b82d906860527fec2c1345e17505946223d125a42b1fc3edf971d3f5583e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **582.5 MB (582511974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77224905c88ce525a4140a5e846305e88afe2509808957c5369474acc2a23d36`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:45:59 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:59 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 14 Apr 2026 20:46:52 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:52 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:46:52 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 14 Apr 2026 20:46:59 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 14 Apr 2026 20:46:59 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 14 Apr 2026 20:46:59 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:59 GMT
ENV SHELL=/bin/bash
# Tue, 14 Apr 2026 20:46:59 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:46:59 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 14 Apr 2026 20:46:59 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 14 Apr 2026 20:46:59 GMT
LABEL org.label-schema.build-date=2026-04-02T10:14:23.779452226Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T10:14:23.779452226Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=cdb2d7a7a46dfe4ef7c3f859b94fb86ba8e652e1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Tue, 14 Apr 2026 20:46:59 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 14 Apr 2026 20:46:59 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:46:59 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 20:46:59 GMT
CMD ["eswrapper"]
# Tue, 14 Apr 2026 20:46:59 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a858d056e2d66c5ae95f64f82e213fec15a052b44f130d3b8bfc61f9373b21`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 4.3 MB (4285298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dce376cc50f33246b46e34d78bf2923cca8e3de0570fb14c8cf0bce4d154fb0`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad5030a4af03ddb063f7bbe2343b725208605bddb31d80cd3a9e03ef82ba44c`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2167bf8f85ba13f8770cbc625be654b2c2e0b65b5a2b6a0667f45d0791eff5a7`  
		Last Modified: Tue, 14 Apr 2026 20:47:49 GMT  
		Size: 539.9 MB (539938119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb32c37fcaebb4b6747b15a756a3a6077d6ff91e07d8153fa806e4a1f0dfff`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115a0cd5633d8675673e7253ac375f492ebdb3baf6e36138375fac288fa600`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016685d5e7d7e8b661e010362a7ad920967e149f4ab5e6ef6be18c5560ae6807`  
		Last Modified: Tue, 14 Apr 2026 20:47:39 GMT  
		Size: 74.1 KB (74110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f693055924ea8fd619f1b0e5dc6836017df4b4a78701d7d51b3300500227bfff`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.2.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:16ebed52289c835b87a382ee035f380b5d6620bd1ae68d05cd108475e55c2db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2132765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316f0849df34f326ceba44500be213173841f39b7cc64a6b09e5591a4b04da88`

```dockerfile
```

-	Layers:
	-	`sha256:4dea030faec0ad4d37ef83191c3e3df5c6b93e78e4125750616391ee300b725f`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 2.1 MB (2098727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aa0329ec2e701191cb1fc473bd2fca67bab99b4f92f70248f780babc704e023`  
		Last Modified: Tue, 14 Apr 2026 20:47:38 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.3.3`

```console
$ docker pull elasticsearch@sha256:84465eca262e3324da194d73eb05acdb9f6c1c8ad877e08790cbf31d5ead226c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.3.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:865fbff3c29559eb850dd2ecb09810a01bc904a5b2a38fa4f808213914bda398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.7 MB (716686135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d5e5b5a0a9d2ba1a799cd7cab27b44ea2c0c7c470c51f7ce0cb6113a0b4310`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:46:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:46:11 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 14 Apr 2026 20:46:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:36 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:46:37 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 14 Apr 2026 20:46:46 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:46:47 GMT
ENV SHELL=/bin/bash
# Tue, 14 Apr 2026 20:46:47 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 14 Apr 2026 20:46:47 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Tue, 14 Apr 2026 20:46:47 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 14 Apr 2026 20:46:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:46:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 20:46:47 GMT
CMD ["eswrapper"]
# Tue, 14 Apr 2026 20:46:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51260130c5a262ccb3b8668c2b8fda2a1f1515915fd5934a1f7dba23b4d09cf3`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 4.3 MB (4277568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcda1dc0bb8662cfe7318aee1759aa35e9802ba61a69b46e5f5bc4480e0f0ed`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 1.5 KB (1540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c8ec364b49a4541a93e7bfa3e3e2de21e814566d4564b3434cbd1488df0e49`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b0b0a10df7ea38dd99e5a7e307442ee79f5d2ea91b0e814bf525478d184cd4`  
		Last Modified: Tue, 14 Apr 2026 20:47:55 GMT  
		Size: 672.3 MB (672302042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f0f9c012831283b7bd04f960fd9cc27ec3a8cc778469d1277f2ab6a930361`  
		Last Modified: Tue, 14 Apr 2026 20:47:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bad7895c2463353dc74235c9392dfffafc6d2bfeedc24754d15ff0cb9fbebe`  
		Last Modified: Tue, 14 Apr 2026 20:47:41 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44c4194af83a91d6608593e8951ab286820f78b78efa18bc94d8e3c5e54cabf`  
		Last Modified: Tue, 14 Apr 2026 20:47:41 GMT  
		Size: 75.2 KB (75178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223f7ad6c6135b61d933027feae40e15f4db8ee04411f309d8ee74f2f38117fa`  
		Last Modified: Tue, 14 Apr 2026 20:47:42 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:034ae79939bfd419d051c14c3b982dbb30657fb1011646ef16c55a2d2604ebf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2123661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d706006f97e9dc044f5a20d53664ac8538694ff0276b4dea5f2219b51ce71b`

```dockerfile
```

-	Layers:
	-	`sha256:a4016b388717da13966b55a3dccd5d2e0bcd0afafd12b766a843e6ed9fdfcd4d`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 2.1 MB (2089805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5cbcc9f6ddbd0352c0f8c3700452548fcce8651c5ed035560921af764bd1b20`  
		Last Modified: Tue, 14 Apr 2026 20:47:40 GMT  
		Size: 33.9 KB (33856 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.3.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:1f5edde83816a744bbc9818cfeb59ebaf80ce8f0be20cdbaa81aa5f2ff123049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.7 MB (560689967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6789551f0f882b2d2b610d6e31a68034d09df43ce3077378f54119e41ec9b533`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:46:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:46:00 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 14 Apr 2026 20:46:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:46:54 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:46:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 14 Apr 2026 20:47:03 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 14 Apr 2026 20:47:03 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 14 Apr 2026 20:47:03 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:47:03 GMT
ENV SHELL=/bin/bash
# Tue, 14 Apr 2026 20:47:03 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:47:03 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 14 Apr 2026 20:47:03 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 14 Apr 2026 20:47:03 GMT
LABEL org.label-schema.build-date=2026-04-01T22:08:18.783399214Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T22:08:18.783399214Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=640408e2dfd2af9fbfe5079e1575f93d8909a5f5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Tue, 14 Apr 2026 20:47:03 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 14 Apr 2026 20:47:03 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:47:03 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 20:47:03 GMT
CMD ["eswrapper"]
# Tue, 14 Apr 2026 20:47:03 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f36b0dd522e208b56a01419ca78d44a06bb2361ec0a975cb69977d45a74159`  
		Last Modified: Tue, 14 Apr 2026 20:47:42 GMT  
		Size: 4.3 MB (4285316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cbe6cd2785ae55de6a987abbf2b32e1e756fe715aad7be04394c2e0e6e36f8`  
		Last Modified: Tue, 14 Apr 2026 20:47:42 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2221c207a10059569aa04d8b67fa4d64ad5611fde668d8de78c92ca60f6e4d92`  
		Last Modified: Tue, 14 Apr 2026 20:47:42 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df2bcd080bb2f2145a685acae7cefef206647c9f1f2c42b7c9ef3a5848de9b5`  
		Last Modified: Tue, 14 Apr 2026 20:47:53 GMT  
		Size: 518.1 MB (518116098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a01b9f5f71b697eec715dc37119c4235f9453adc8377a7ea3386e675d9de25`  
		Last Modified: Tue, 14 Apr 2026 20:47:43 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53ed6bb14d35209ac86b374f03e9b149796226aa4cb878013f3ea136a259289`  
		Last Modified: Tue, 14 Apr 2026 20:47:43 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913b0d57963577b1454bfa576347bbe6bc079b87e5db9109037d703d57f14991`  
		Last Modified: Tue, 14 Apr 2026 20:47:43 GMT  
		Size: 74.1 KB (74105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf4d86f9d6ac4a382310a6a5329d6c97cc8c6c563ebf4203cd8bee577ab1e40`  
		Last Modified: Tue, 14 Apr 2026 20:47:44 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.3.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9d5cb097b107aebfa6ddc2743a7bf1ee169f257676719020a87288d06b882dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2124405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c454ce3c21ff94e24ab9b15769245abe40d348771c7e910b5fcf24c29c3b623b`

```dockerfile
```

-	Layers:
	-	`sha256:99dd274310eb876866ae17585462bc30d40ce919713fc34e2aae99b621fb6319`  
		Last Modified: Tue, 14 Apr 2026 20:47:42 GMT  
		Size: 2.1 MB (2090367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d301e4ecac93079d79b1e6c35b6636f70f2da8f8d984085571d485c325d8e027`  
		Last Modified: Tue, 14 Apr 2026 20:47:41 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json
