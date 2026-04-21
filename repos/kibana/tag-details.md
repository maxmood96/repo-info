<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.14`](#kibana81914)
-	[`kibana:9.2.8`](#kibana928)
-	[`kibana:9.3.3`](#kibana933)

## `kibana:8.19.14`

```console
$ docker pull kibana@sha256:82d68785303fb6934a0f74b8b50f81d4ba2267a245edd6a311d59413eecd84e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.14` - linux; amd64

```console
$ docker pull kibana@sha256:177134229c34f6dc85573e531d57731aeea1093dfed2c0e62f988a5d00358786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.3 MB (442291760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3845c6fc6b559998798fe9dd0c125b666c48e4a3d10f376cfb286bb1085a89be`
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
# Wed, 15 Apr 2026 20:43:41 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 15 Apr 2026 20:43:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:52:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 15 Apr 2026 20:52:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 15 Apr 2026 20:52:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 15 Apr 2026 20:52:28 GMT
RUN fc-cache -v # buildkit
# Wed, 15 Apr 2026 20:52:28 GMT
WORKDIR /usr/share/kibana
# Wed, 15 Apr 2026 20:52:28 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 15 Apr 2026 20:52:28 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Apr 2026 20:52:28 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:52:28 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 15 Apr 2026 20:52:28 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:52:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 15 Apr 2026 20:52:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 15 Apr 2026 20:52:29 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 15 Apr 2026 20:52:29 GMT
LABEL org.label-schema.build-date=2026-04-02T14:20:50.138Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T14:20:50.138Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 15 Apr 2026 20:52:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 15 Apr 2026 20:52:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 15 Apr 2026 20:52:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bdab5b19f715d063ce1a0bf71ff8145e9929992c41fd3b82b2a125e814abcd`  
		Last Modified: Wed, 15 Apr 2026 20:53:25 GMT  
		Size: 9.4 MB (9434355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bbf1680123ac916d007e7269935a0134b457375a1ec21cecc6fb0fe2c408c4`  
		Last Modified: Wed, 15 Apr 2026 20:53:34 GMT  
		Size: 386.5 MB (386480429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd21a01580c8093a157ba3e70786f39a4fc93eff15e60e9534304daf263d121`  
		Last Modified: Wed, 15 Apr 2026 20:53:25 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8175448a143649ff430304a7f4ad36f2c9ffffd445a5f7d785aff5752bd474`  
		Last Modified: Wed, 15 Apr 2026 20:53:26 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882172abe9904881c42659078e70e1fa1f6af3b348c3670964e2adee738658e4`  
		Last Modified: Wed, 15 Apr 2026 20:53:26 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593e0beca21579c59485e3a6678097c67a3a980bfe616d4b9c767002d796bffb`  
		Last Modified: Wed, 15 Apr 2026 20:53:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099e49d3a9dd614aa343104f31c738840546291d90520032dd6f2a2789d42a3b`  
		Last Modified: Wed, 15 Apr 2026 20:53:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4679f9c345b615aae00270fd1a3e9fa064d8e9ed9d957ac3380d376129f594aa`  
		Last Modified: Wed, 15 Apr 2026 20:53:27 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614c84822ee8a5f40986e1c27061960d3acbf7e7e5f215c7e07f556368e09ec1`  
		Last Modified: Wed, 15 Apr 2026 20:53:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c00fc1af89bc5d6de78c633a24025f5e953d431876f1684897ac6935a253aeb`  
		Last Modified: Wed, 15 Apr 2026 20:53:29 GMT  
		Size: 161.7 KB (161738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056edc0d8f6bdc847b44b33573bbc61c3351654f57e15827b045e0f213ffd224`  
		Last Modified: Wed, 15 Apr 2026 20:53:29 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.14` - unknown; unknown

```console
$ docker pull kibana@sha256:78ca4b15d007692a48aa711c5c037f26d968efff40de850eec5ae0065a24dee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff42fc3a07c5ad529ffe66303a0b502ff9b1db3c64b7789da50996a2d5bc733`

```dockerfile
```

-	Layers:
	-	`sha256:162d84a302fd717cf8537c83f7be69a545e7a7f32b7fd43aad69f2a48b787eed`  
		Last Modified: Wed, 15 Apr 2026 20:53:25 GMT  
		Size: 4.9 MB (4931399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff296543b56a23a24a903ae6a6b20ecfe28980bb4f7adfd3f7e36eaa6f02ee08`  
		Last Modified: Wed, 15 Apr 2026 20:53:25 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.14` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8c6600701b9b36ec2a4a534407d5eea9a50227f4cc1b42d24f99f07fdfaf9525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.2 MB (455194579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f38bd5ffd4b679097f759ecd752f4d222663a409bd73b58e0e927c6f7e9b9c`
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
# Wed, 15 Apr 2026 20:43:59 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 15 Apr 2026 20:43:59 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:51:07 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 15 Apr 2026 20:51:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 15 Apr 2026 20:51:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 15 Apr 2026 20:51:08 GMT
RUN fc-cache -v # buildkit
# Wed, 15 Apr 2026 20:51:08 GMT
WORKDIR /usr/share/kibana
# Wed, 15 Apr 2026 20:51:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 15 Apr 2026 20:51:08 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 15 Apr 2026 20:51:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:51:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 15 Apr 2026 20:51:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:51:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 15 Apr 2026 20:51:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 15 Apr 2026 20:51:10 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 15 Apr 2026 20:51:10 GMT
LABEL org.label-schema.build-date=2026-04-02T14:20:50.138Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T14:20:50.138Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 15 Apr 2026 20:51:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 15 Apr 2026 20:51:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 15 Apr 2026 20:51:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24ece901abeca72f5a5e16332ca8febdd5e358c46bd28752b28b740d4ec098d`  
		Last Modified: Wed, 15 Apr 2026 20:52:15 GMT  
		Size: 9.5 MB (9451944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bd19e6bee803860a4f31844c632f25276f794f8a801de885cb2312282e5ab4`  
		Last Modified: Wed, 15 Apr 2026 20:52:23 GMT  
		Size: 400.2 MB (400226765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b574ba0c43501aa6a6378821f87588ebf00d4004174fe6504f2101fc365c94`  
		Last Modified: Wed, 15 Apr 2026 20:52:15 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84369dbef114d8ac0f2e04c59b1ef0259370bba20d2509be70486cf01f71bc5`  
		Last Modified: Wed, 15 Apr 2026 20:52:16 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e17e7d5b9c45f7700b55a89e5bc16b2b0899439d5eeaaa8e00631cef1eab87a`  
		Last Modified: Wed, 15 Apr 2026 20:52:16 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5c694391d0f0a776ebb8c3752b1b379eb81c985c834a066ad60c9c9eb417d`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfb219045687deb15ae0a45c38270777e469682068c6d3f42e626823b8e2777`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e2992579cd32e88858e919988160b77f6050ae5c641929a864c8a3c2c785b`  
		Last Modified: Wed, 15 Apr 2026 20:52:17 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540c04e1c506732d31385463e06a8b807072738d9947d620110c6cec8d4fc000`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c37d18f15fbb2cc9dcaa2f4f09e4e04ed7eb2fd047ebbae93b2643867db3d0b`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 158.3 KB (158258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ba116047445d2c45b1a40e5f8b2cf7af5712dcd7a685ad8a8accffed661a0d`  
		Last Modified: Wed, 15 Apr 2026 20:52:18 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.14` - unknown; unknown

```console
$ docker pull kibana@sha256:d8d453cb4cacc99ea1d2272ddb5560b0671fa77b65fc79688878ac15c5085496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c3d4a5d3b0306d26c0e2f1c95ceddf23409c146cbc2ad5f224b2f28bba288b`

```dockerfile
```

-	Layers:
	-	`sha256:161874dd3a7b1c51c9552685a16fa3841f2fc20eafb666ce2683be7b52529ced`  
		Last Modified: Wed, 15 Apr 2026 20:52:15 GMT  
		Size: 4.9 MB (4932463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9423f8cfaec39c6516c9b28aee3ca0049ab163040b5b46dae3c6caf9c4e3ca`  
		Last Modified: Wed, 15 Apr 2026 20:52:14 GMT  
		Size: 41.2 KB (41162 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.8`

```console
$ docker pull kibana@sha256:ca5dd1086368ba41ddd20baabc02e543b798b0554a3f37f930a6dad863ea0ac8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.8` - linux; amd64

```console
$ docker pull kibana@sha256:8759cd57911e5e17d27a1965f1fd6df1bf228139564bc3eab037429b9ae3043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447857362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8311c1eaf9f9129069c88317d492692178e24506ba58f639ac06cfe58cd4c9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 20 Apr 2026 23:07:04 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 20 Apr 2026 23:07:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:15:55 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 20 Apr 2026 23:15:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:15:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 20 Apr 2026 23:15:56 GMT
RUN fc-cache -v # buildkit
# Mon, 20 Apr 2026 23:15:56 GMT
WORKDIR /usr/share/kibana
# Mon, 20 Apr 2026 23:15:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 20 Apr 2026 23:15:56 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:15:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:15:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 20 Apr 2026 23:15:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 20 Apr 2026 23:15:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 20 Apr 2026 23:15:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 20 Apr 2026 23:15:58 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Mon, 20 Apr 2026 23:15:58 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 20 Apr 2026 23:15:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:15:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 20 Apr 2026 23:15:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 20 Apr 2026 23:15:58 GMT
USER 1000
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d729cf5c12ee164b4b3b5225840a2c5a918679822873e621f72e1d0d987346`  
		Last Modified: Mon, 20 Apr 2026 23:16:55 GMT  
		Size: 19.5 MB (19521382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ff3610ceabe7d3a743977636886029332141479a96eb17aa2493d4041f101e`  
		Last Modified: Mon, 20 Apr 2026 23:17:04 GMT  
		Size: 371.8 MB (371761309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d084304466e6dbfb5d93a3707dd14def224c64299e667eab3d947ebb1ce92`  
		Last Modified: Mon, 20 Apr 2026 23:16:53 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369689cd993c35ab0437ac980312bfd27858cbce39d822364a0acac8e27f763`  
		Last Modified: Mon, 20 Apr 2026 23:16:55 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9ad380c20059a294856e836a9e23dd11065e7b28b927a709964b12ca603e79`  
		Last Modified: Mon, 20 Apr 2026 23:16:55 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe24132f1de50e5d662ff4055d7647036861d4341c7ae2265fb797d4af16b6f`  
		Last Modified: Mon, 20 Apr 2026 23:16:56 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fbc7758bef4d692fb22cb3c39e4b5b9d67d97b5d502254d42a84771cd1a204`  
		Last Modified: Mon, 20 Apr 2026 23:16:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b500a5e331e365b802b0665f580674320c12e2fd990dd30df96e370dbe1e46`  
		Last Modified: Mon, 20 Apr 2026 23:16:57 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db1a9c22974f39c3ae26466f0772891fe0b4c585cf6b46a2d14daf6eebb5792`  
		Last Modified: Mon, 20 Apr 2026 23:16:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc789f3a3e9ac12f39c0ddf57e8cf5e7e32a887114b3ef8833479e79e413bbb`  
		Last Modified: Mon, 20 Apr 2026 23:16:58 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f738cc4257568337479a9accbccaad3aa848ad30d26eee42c1aeef3c71206`  
		Last Modified: Mon, 20 Apr 2026 23:16:58 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321d6440774d30a7d56dc1f3bc22d9adc4822db757814c68dbc68093de53ec2d`  
		Last Modified: Mon, 20 Apr 2026 23:16:59 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:fc4e1a32388b685e21c93d17a0f70a9356c8de31b3644587318dc492e43ffde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1999af4dca04182cf44210146f2f109ff230f75210e4866e75f9849231ec929`

```dockerfile
```

-	Layers:
	-	`sha256:c081c6d18d3eae007d787cb5651fb5d6a8566404a2ef4d3662c9b28df2f6f846`  
		Last Modified: Mon, 20 Apr 2026 23:16:54 GMT  
		Size: 5.7 MB (5730216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a769a73876660452f052f4edf0b497fd4c1c8ecd73390fd8cd0a9a6b49807a54`  
		Last Modified: Mon, 20 Apr 2026 23:16:54 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:cbb8370685e0dc1ddffe7bfd94d7dac980698059048201c80f768f90e59fb58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.7 MB (459719795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc53fd094d1ae7a2183abf3722b1873017827523df33bd6ded672ae3f9e937`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 20 Apr 2026 23:04:41 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 20 Apr 2026 23:04:41 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:11:45 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 20 Apr 2026 23:11:45 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:11:45 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 20 Apr 2026 23:11:46 GMT
RUN fc-cache -v # buildkit
# Mon, 20 Apr 2026 23:11:46 GMT
WORKDIR /usr/share/kibana
# Mon, 20 Apr 2026 23:11:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 20 Apr 2026 23:11:46 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:11:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:11:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 20 Apr 2026 23:11:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:11:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 20 Apr 2026 23:11:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 20 Apr 2026 23:11:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 20 Apr 2026 23:11:48 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Mon, 20 Apr 2026 23:11:48 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 20 Apr 2026 23:11:48 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:11:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 20 Apr 2026 23:11:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 20 Apr 2026 23:11:48 GMT
USER 1000
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1406c461cd6cc8cc599661e7780db8b934aa268db8b530004002a4f1e001523`  
		Last Modified: Mon, 20 Apr 2026 23:12:52 GMT  
		Size: 19.5 MB (19476009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05af1f98b6c2299194383eaf82402ad0ef1b11b3470bc4b5a52457f5ea5e4978`  
		Last Modified: Mon, 20 Apr 2026 23:12:59 GMT  
		Size: 385.5 MB (385486802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c96f1200cc6893651cb1d7181651aad47e75e20fc3da1c7caf6cb867e86a623`  
		Last Modified: Mon, 20 Apr 2026 23:12:50 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c904edfaddee12ea0a32adaeda8d6718ca3f02bbe27a55e1e0a0873a0cf07f5`  
		Last Modified: Mon, 20 Apr 2026 23:12:52 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd808abfef37d558d4d585410b65467df24ef7fa740ee16c756a447cf564d12f`  
		Last Modified: Mon, 20 Apr 2026 23:12:52 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82b20256fa6fa2c581250826fb4c72bd2bb55b67bc10b8a942363705007d04b`  
		Last Modified: Mon, 20 Apr 2026 23:12:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8372de9b19d01df92f59975ddc509e1ed9a987da555c5b96ff3f3c4e79fdd6`  
		Last Modified: Mon, 20 Apr 2026 23:12:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b12bffda787ae71ee8a42cf430d09a0d0170b6b1709dbabf7703c3a81dc55a`  
		Last Modified: Mon, 20 Apr 2026 23:12:53 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da11b1a1e75896dc99220e7ca7afa9640b6eb18cd97325b390c6bd9f6d0128fe`  
		Last Modified: Mon, 20 Apr 2026 23:12:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b02c8a27485a0a28ec0e8cdf1795a86d1fd341f1533e34effcafbc96198189`  
		Last Modified: Mon, 20 Apr 2026 23:12:55 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0fe91ff9502ff0ad248c4094625c2274bc241b56628e3b4e08ee49444ca96c`  
		Last Modified: Mon, 20 Apr 2026 23:12:55 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aaa2b28636d712ab4385cd5ba752169e700ea543013163d4bac8af306ec740e`  
		Last Modified: Mon, 20 Apr 2026 23:12:56 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:37c3fa85fcf3bf8a1f850933fea16c80a7f726235a138265c8bc029dd52454cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46e70f9bdce8125d62b4a7d97ef36254b76db2ec98231f1d60037f76f7daa68`

```dockerfile
```

-	Layers:
	-	`sha256:4dac265be9ad8bfdc1938209dab8e881a08e47280b014e81156eca8751327a6c`  
		Last Modified: Mon, 20 Apr 2026 23:12:51 GMT  
		Size: 5.7 MB (5728888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c21ff388895d8278a43d138723587c926cfe2eff2ee54887753b06fed4d0197`  
		Last Modified: Mon, 20 Apr 2026 23:12:51 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.3`

```console
$ docker pull kibana@sha256:dc3f0bd87a335a5599be88e5976448be9bf91e75a628ab869a7fd004c8c35964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.3` - linux; amd64

```console
$ docker pull kibana@sha256:1c62f3497735fbfd97082ccb01fd4aebce64daa6c5613793ca66e7c7fd978b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453165576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040c7dbc27b38df4e943a35ee00009ad6e62808a150e0144781f7a5e64cc7186`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 20 Apr 2026 23:07:04 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 20 Apr 2026 23:07:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:16:31 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 20 Apr 2026 23:16:31 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:16:32 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 20 Apr 2026 23:16:32 GMT
RUN fc-cache -v # buildkit
# Mon, 20 Apr 2026 23:16:32 GMT
WORKDIR /usr/share/kibana
# Mon, 20 Apr 2026 23:16:32 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 20 Apr 2026 23:16:32 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:16:32 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:16:32 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 20 Apr 2026 23:16:32 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:16:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 20 Apr 2026 23:16:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 20 Apr 2026 23:16:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 20 Apr 2026 23:16:34 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Mon, 20 Apr 2026 23:16:34 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 20 Apr 2026 23:16:34 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:16:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 20 Apr 2026 23:16:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 20 Apr 2026 23:16:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65a1ab5671fa3ba18fc77180fa167ce4c383110957a7744bfe3ae0143a5e900`  
		Last Modified: Mon, 20 Apr 2026 23:17:34 GMT  
		Size: 19.5 MB (19521378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23657730f9b2a95365717cdb02cf39ab5bf2a03379d6dbacbf0f90c7970b9e97`  
		Last Modified: Mon, 20 Apr 2026 23:17:42 GMT  
		Size: 377.1 MB (377069493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e6df20bde71a516d0d2ba6623636a38e46274d2a48262b01fca65116ba33a8`  
		Last Modified: Mon, 20 Apr 2026 23:17:33 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6320ba99fbcd33540681fbef961228e835b72c2cb9d991e8dfcbf1347d1b58c4`  
		Last Modified: Mon, 20 Apr 2026 23:17:34 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f9e180981d38c5bb47b936c39fb346d09b4651bbea8f0619c4ced87f9235bc`  
		Last Modified: Mon, 20 Apr 2026 23:17:34 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c960e56d0d6d3f2587b53e9effa54cd961b169acfbd1f43eb7928fd1cce088d4`  
		Last Modified: Mon, 20 Apr 2026 23:17:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c1435017e3ddce87397001148edf2e6806d51405ba9a0a3c3b3355274c08c3`  
		Last Modified: Mon, 20 Apr 2026 23:17:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f3c6c27f49623ebb78f465b9665fce78c2b83f4c565f2c8f22e3f8cbf7d833`  
		Last Modified: Mon, 20 Apr 2026 23:17:36 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91c14b3c13bb082652ca36a98ec9783a0c27ef8774953000065283ff62da012`  
		Last Modified: Mon, 20 Apr 2026 23:17:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7302040b4b22e0d5adf260716db4ea005a4bc7e5126ca365cca65f98989ad2ad`  
		Last Modified: Mon, 20 Apr 2026 23:17:37 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f9d2895b2e417338d7ddcdcc4d5a1c88bd5bda0e948892a273494c01c1c8ce`  
		Last Modified: Mon, 20 Apr 2026 23:17:37 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f91f02227589683f3387648c72931fd99b4a3ec94e2939c2b13584156e437`  
		Last Modified: Mon, 20 Apr 2026 23:17:39 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:2e7e2a50f3027133c1ff3d2b98af2564e45ddce34e04a95a9ae0db63b295062a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d60ccc01b7d82ea7beb3e5fae2551eb3c575d24cf339be947c79077974f9ee6`

```dockerfile
```

-	Layers:
	-	`sha256:e04fbc30550380c7010ffe853f56cdf902999b25f79916cd6f2a89af4239f467`  
		Last Modified: Mon, 20 Apr 2026 23:17:33 GMT  
		Size: 5.8 MB (5794135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0a62a2de8e85de0d17a670d21a3946c190cacbae27584b077f788411b120f0`  
		Last Modified: Mon, 20 Apr 2026 23:17:33 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4e74b2e92f9b5222326131d5c893ed0dff53fcf06cedabb7b896222da66a6279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.1 MB (465068908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdfe9b9cb7cec7ffb5c46456121fd4cd3d4104e04f0278e8b618afdd0ff2ad3`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Mon, 20 Apr 2026 23:04:52 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 20 Apr 2026 23:04:52 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:12:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 20 Apr 2026 23:12:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 20 Apr 2026 23:12:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 20 Apr 2026 23:12:12 GMT
RUN fc-cache -v # buildkit
# Mon, 20 Apr 2026 23:12:12 GMT
WORKDIR /usr/share/kibana
# Mon, 20 Apr 2026 23:12:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 20 Apr 2026 23:12:12 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 20 Apr 2026 23:12:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:12:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 20 Apr 2026 23:12:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 20 Apr 2026 23:12:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 20 Apr 2026 23:12:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 20 Apr 2026 23:12:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 20 Apr 2026 23:12:14 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Mon, 20 Apr 2026 23:12:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 20 Apr 2026 23:12:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 20 Apr 2026 23:12:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 20 Apr 2026 23:12:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 20 Apr 2026 23:12:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e213b83170541d02fa0b242b5a64f2048b2f13dfc5e74b322e853f6debbb06fc`  
		Last Modified: Mon, 20 Apr 2026 23:13:19 GMT  
		Size: 19.5 MB (19476049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357dff3b20d609a3d49a813a453949c732cbaa95fb2f091bd01a54e772e58d6e`  
		Last Modified: Mon, 20 Apr 2026 23:13:25 GMT  
		Size: 390.8 MB (390835850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b293afe218d4e7711cb0a4f2533d20b6acaf1bc0a8295d69f1c1f0b8bf1233be`  
		Last Modified: Mon, 20 Apr 2026 23:13:17 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0273726effbc753dd83a7e7f8f1236eddec698b06a5446f14a418a9a8a75f9a0`  
		Last Modified: Mon, 20 Apr 2026 23:13:18 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f333c2d5b3cc3b7a82355fefcf644660289c402045b6608b13aa63041fd1006c`  
		Last Modified: Mon, 20 Apr 2026 23:13:18 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580336eff002827f2171a15f7b2baf89c7bb2d36d67f7c517acf3da96ed71b1f`  
		Last Modified: Mon, 20 Apr 2026 23:13:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a441a028f2f340a78eb46d605794c033d611f82d729d2789ba8420089b45d7f2`  
		Last Modified: Mon, 20 Apr 2026 23:13:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfea77114fc542cb97fc38170d9c74ac0590628f33864b8fff543bfc494b3d0`  
		Last Modified: Mon, 20 Apr 2026 23:13:20 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8429415c5c248dc2edc5d294aee97410cd6084d40c890174375179365398ae76`  
		Last Modified: Mon, 20 Apr 2026 23:13:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a423ec75b37a97bd44157d2c46fb9272782762eca26adeee57223c0c1d56e`  
		Last Modified: Mon, 20 Apr 2026 23:13:22 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ae87a8b119ffd5b588adbe26aa245e266129408e7f251bfb97d273be2d8769`  
		Last Modified: Mon, 20 Apr 2026 23:13:22 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6976df5ac98ff449dd43c33ac5e24f35863d2b81598cf4793ec2acba28ed424c`  
		Last Modified: Mon, 20 Apr 2026 23:13:22 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:368b75270c417eb958106bdd88e77f57792573bf75db7d33faf4360a0046b929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5836290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87ad53191ec422410063acf9969b6878ce6dbeececc5f5da68af82f05a8a900`

```dockerfile
```

-	Layers:
	-	`sha256:44b32b030f65f49aa3204caec4bbff21e3a472aa27ff838d3acff3b4b354147a`  
		Last Modified: Mon, 20 Apr 2026 23:13:18 GMT  
		Size: 5.8 MB (5792807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b8346d51521d2cfa6ebc5d2ef67220d90930d519fb7ad4e4825692b3f4eb82`  
		Last Modified: Mon, 20 Apr 2026 23:13:17 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
