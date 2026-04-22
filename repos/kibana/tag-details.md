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
$ docker pull kibana@sha256:26ba0a5c1fce9d1b3a92e952020cba6b028cb8c29d8ba8a7574ef188c3467b4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.8` - linux; amd64

```console
$ docker pull kibana@sha256:53ec77fadeb480c5d294f2e7dc3ce20b51a63687ef7cd8e306bbd14d74a8bf6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447860790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fb17ee41b5e3d1d9df10edcc0e4a8ca6b838bd4e4d281b454e88b03b212e07`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Wed, 22 Apr 2026 18:17:45 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 22 Apr 2026 18:17:45 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:26:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 22 Apr 2026 18:26:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:26:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 22 Apr 2026 18:26:51 GMT
RUN fc-cache -v # buildkit
# Wed, 22 Apr 2026 18:26:51 GMT
WORKDIR /usr/share/kibana
# Wed, 22 Apr 2026 18:26:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 22 Apr 2026 18:26:51 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:26:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:26:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 22 Apr 2026 18:26:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:26:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 22 Apr 2026 18:26:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 22 Apr 2026 18:26:53 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 22 Apr 2026 18:26:53 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 22 Apr 2026 18:26:53 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 22 Apr 2026 18:26:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:26:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 22 Apr 2026 18:26:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 22 Apr 2026 18:26:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598749e4c0b0916670638b5b371be3930de6f96d2caa0e7a7cdb8529d35b1c27`  
		Last Modified: Wed, 22 Apr 2026 18:27:52 GMT  
		Size: 19.5 MB (19518947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5c22bfc9931aa8061b4177225811bbd0add2c311c5757d165e930a15c656df`  
		Last Modified: Wed, 22 Apr 2026 18:27:59 GMT  
		Size: 371.8 MB (371758685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b970882de0b13f3b3e7242b681db9ccb8302a25371614b3155964b944f5773`  
		Last Modified: Wed, 22 Apr 2026 18:27:51 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258aa545071618d41f82e22c2816a2d7dfd20cbc6727b9f207aeb9760bb1ed7d`  
		Last Modified: Wed, 22 Apr 2026 18:27:52 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20bc23ae987310988d1fd401071bce032680da2db041bc76595b6c570e64bd0`  
		Last Modified: Wed, 22 Apr 2026 18:27:52 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37849aa529b2f9b1e41774421722172ccbee92a3b2ee8b18f42d70a9af667b6`  
		Last Modified: Wed, 22 Apr 2026 18:27:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bea8d56174d273383f4bce17a8e7059b98b88c6f479aa76a6447070aaef2a9`  
		Last Modified: Wed, 22 Apr 2026 18:27:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a74a68ecd6615359151946785f93bafdeb6709c179cc08827472b7a9f873a4`  
		Last Modified: Wed, 22 Apr 2026 18:27:54 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f4e0c863c714923f5e965a3d75de92885f118d4bc2577de9745430d3fb1252`  
		Last Modified: Wed, 22 Apr 2026 18:27:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817614e05bf07ba8fcc43f4b06ea4d4608b4acd3cd2d40794e36f71384aea5f7`  
		Last Modified: Wed, 22 Apr 2026 18:27:55 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd554c692b8f1c2242f7617844616e74c00bb3aea6a6ff6c7f34009fbd1c7c61`  
		Last Modified: Wed, 22 Apr 2026 18:27:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ddaa03770394b87e27ffc784f9014b337351d4d418635ee0dfdfca6768d9b4`  
		Last Modified: Wed, 22 Apr 2026 18:27:56 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:997f7180b353b3b9689fed6f7e6e982973083b3ee9ae941f6acbb84396856151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a733d96153c3a0fe82f38fa53a82e98ed60a9003f6cb8f424d7987d3250ceb`

```dockerfile
```

-	Layers:
	-	`sha256:1812c63f449fe4c956cc737b170cc3bada0db47a0d3ea9df720b3e8ecbc61c82`  
		Last Modified: Wed, 22 Apr 2026 18:27:51 GMT  
		Size: 5.7 MB (5730216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a737670b3903a75bca60f56041c50f7e884d8217f2f2983a16f80c414228ed79`  
		Last Modified: Wed, 22 Apr 2026 18:27:51 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:419ff613740b5efc551017d2c686c5bff25eadbc8bfc4ca56106527244d1c1e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.7 MB (459730604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4526f44a9153e5808cc6ea4c70228cca72fc96fd213d92193387af482e3b3aaa`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Wed, 22 Apr 2026 18:17:13 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 22 Apr 2026 18:17:13 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:24:39 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 22 Apr 2026 18:24:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:24:40 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 22 Apr 2026 18:24:40 GMT
RUN fc-cache -v # buildkit
# Wed, 22 Apr 2026 18:24:40 GMT
WORKDIR /usr/share/kibana
# Wed, 22 Apr 2026 18:24:40 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 22 Apr 2026 18:24:40 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:24:40 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:24:40 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 22 Apr 2026 18:24:40 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:24:41 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 22 Apr 2026 18:24:42 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 22 Apr 2026 18:24:42 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 22 Apr 2026 18:24:42 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 22 Apr 2026 18:24:42 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 22 Apr 2026 18:24:42 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:24:42 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 22 Apr 2026 18:24:42 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 22 Apr 2026 18:24:42 GMT
USER 1000
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0706d52c928890942cc4d518cab11a25ed421a4878d0608beee39798e456bd`  
		Last Modified: Wed, 22 Apr 2026 18:25:46 GMT  
		Size: 19.5 MB (19476156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68868d7b198372fdcdbe1a7698c7a767b1b5ba3ba35418e4022d70ba666f12a`  
		Last Modified: Wed, 22 Apr 2026 18:25:54 GMT  
		Size: 385.5 MB (385493086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f70fd641156457c5d1cd4c7a700b8687dff3a9be4a48d84227e6b968ce6b6d`  
		Last Modified: Wed, 22 Apr 2026 18:25:45 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b443a102d36d656af3fae1d941811033a5e7a8c889e3da99b696b69e7645cf1`  
		Last Modified: Wed, 22 Apr 2026 18:25:46 GMT  
		Size: 16.5 MB (16460499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e53e3ac8cb3a231a668760f7c5f120fe8946ae0292d7945bc8398650d9d795`  
		Last Modified: Wed, 22 Apr 2026 18:25:46 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cf063481f3d6a549534ee855dfd73b56dd821af5773cf7721b592e41320955`  
		Last Modified: Wed, 22 Apr 2026 18:25:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3dbbac9ba23330ab322bf41373322c245fcf6bf653d41174bf51f3a2792bba`  
		Last Modified: Wed, 22 Apr 2026 18:25:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e6af63fa429164d872c1d9a9ed6df527f332fd74411a54a9e73e7647f5384b`  
		Last Modified: Wed, 22 Apr 2026 18:25:48 GMT  
		Size: 4.9 KB (4891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e03671ad7d80e7e5dd25ebe96224f2e36736e0356d8aefb095605eee24c08f`  
		Last Modified: Wed, 22 Apr 2026 18:25:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8ea22bbc0c8c4542f673d50173e4c51801f503b7a3f8acd34946fd34b08e87`  
		Last Modified: Wed, 22 Apr 2026 18:25:49 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bbb796ff9405563569e3bc2411bf73481f2e6eec4cf6dfd8feca5ffad5810d`  
		Last Modified: Wed, 22 Apr 2026 18:25:49 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fffd043d75d1a8c062558f1a00ec01e375cb315985fe9af364b7f1de9f1743`  
		Last Modified: Wed, 22 Apr 2026 18:25:51 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:b9ae3c7747eb2081e01eddf0874e16ecac8c69d528bf723a2b87e73b31ebc2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd4428d058e513d8cc0b52d164e6be9c0a2f5a67d7db59288a8f0aaaabd4ea6`

```dockerfile
```

-	Layers:
	-	`sha256:b3ee965c4505ac2e2a373c87986cef5df4f792bb75160a3078575150fa60ca16`  
		Last Modified: Wed, 22 Apr 2026 18:25:45 GMT  
		Size: 5.7 MB (5728888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6af3a6d145849b49af0522048b0663c66ba6fe455a415dc9646a0e2b633cfe7`  
		Last Modified: Wed, 22 Apr 2026 18:25:45 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.3`

```console
$ docker pull kibana@sha256:7eb49c105e45085b1d44d0e78ceb152e479432b68a8a8f2dd71abe128eaa9b7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.3` - linux; amd64

```console
$ docker pull kibana@sha256:379bc98744df10df04ceeaccd89c0b7cef0c643c63250f656615c76ec0970b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453188183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae59fb4b1db469bb62c6a80a1eed6041bc2afe68ec4f1be02a09b66227ff6044`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Wed, 22 Apr 2026 18:17:55 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 22 Apr 2026 18:17:55 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:27:23 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 22 Apr 2026 18:27:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:27:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 22 Apr 2026 18:27:24 GMT
RUN fc-cache -v # buildkit
# Wed, 22 Apr 2026 18:27:24 GMT
WORKDIR /usr/share/kibana
# Wed, 22 Apr 2026 18:27:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 22 Apr 2026 18:27:24 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:27:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:27:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 22 Apr 2026 18:27:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:27:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 22 Apr 2026 18:27:25 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 22 Apr 2026 18:27:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 22 Apr 2026 18:27:25 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 22 Apr 2026 18:27:25 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 22 Apr 2026 18:27:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:27:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 22 Apr 2026 18:27:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 22 Apr 2026 18:27:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf0a5487043a9ba5fbf652a3de58906beb8b84d4f50db9869096aef37e8856`  
		Last Modified: Wed, 22 Apr 2026 18:28:22 GMT  
		Size: 19.5 MB (19518884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e576153d2e5673a508d9486723d7ed50213bb25ecfecaa0ec2d2377b00c58`  
		Last Modified: Wed, 22 Apr 2026 18:28:29 GMT  
		Size: 377.1 MB (377086112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b444dfea61e40953ee57fd73994174ec8cbbc8820ec243804b1641e14f162`  
		Last Modified: Wed, 22 Apr 2026 18:28:21 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43aeaae139859cd865d195e5a3cd6202010e5dad85fe2335c149ce4de6f2fb6d`  
		Last Modified: Wed, 22 Apr 2026 18:28:22 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24f0d35990fc73dd606c3b4e796995137cc3fe751ea3a97bc180a67230cc8b6`  
		Last Modified: Wed, 22 Apr 2026 18:28:22 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032e1be45f88bf4909476a4e9ad128f2464f38e8994bf34ba4c140d29e1c89f8`  
		Last Modified: Wed, 22 Apr 2026 18:28:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd305b8e64408db583a166fc850a7524039bfe66ca9b6f4fe519c6bb95b73725`  
		Last Modified: Wed, 22 Apr 2026 18:28:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d42be1710c1d5232c808e4fe67b6996ea1b22894cc5ca1ab6945a5ebdb3cd`  
		Last Modified: Wed, 22 Apr 2026 18:28:24 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ead1ca0993ebd07694f78825e11fc4a6cd438e05540c91edb18c14f498d5a7`  
		Last Modified: Wed, 22 Apr 2026 18:28:25 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b97d14e2c41e4d9ec05a6930108cb4f97ca00d2f88a6786cbb56324f488f8b`  
		Last Modified: Wed, 22 Apr 2026 18:28:25 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d9ad683fbf919bb6500825524c42e44ec4b387a5c6627fd8dd442d57ce337`  
		Last Modified: Wed, 22 Apr 2026 18:28:25 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d98584e41583b1a69aefe0add6988d7855a223ecefd9274f913179ce9717c0`  
		Last Modified: Wed, 22 Apr 2026 18:28:26 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:6bf7595c6298ebaf68b84504e309a762a66e5c7ea18cae3a21203cf51959abfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54efffeb75f043da0f7df7dd97ecfec4accca84843a1bfb7dccb985622a843c`

```dockerfile
```

-	Layers:
	-	`sha256:6a612f0abfd74f045fd87e59e935365ce37aa17c7de9170be521dcf85c02b3ee`  
		Last Modified: Wed, 22 Apr 2026 18:28:21 GMT  
		Size: 5.8 MB (5794135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c087826f5988e5a82a9bd4676e9c20ebda3102bc29c55e3204190a3ce4ce2ca5`  
		Last Modified: Wed, 22 Apr 2026 18:28:21 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1404a8105e2495b518925dbc59ed79c5e39088feb638773bdcc241dad1060d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.1 MB (465062283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e0b51c879e0161c6f6e33e7ec202f793ab6dfe4088e6e4e855af7654643da9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Wed, 22 Apr 2026 18:17:12 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 22 Apr 2026 18:17:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:24:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 22 Apr 2026 18:24:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 22 Apr 2026 18:24:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 22 Apr 2026 18:24:55 GMT
RUN fc-cache -v # buildkit
# Wed, 22 Apr 2026 18:24:55 GMT
WORKDIR /usr/share/kibana
# Wed, 22 Apr 2026 18:24:55 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 22 Apr 2026 18:24:55 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 22 Apr 2026 18:24:55 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:24:55 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 22 Apr 2026 18:24:55 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 18:24:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 22 Apr 2026 18:24:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 22 Apr 2026 18:24:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 22 Apr 2026 18:24:57 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 22 Apr 2026 18:24:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 22 Apr 2026 18:24:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 22 Apr 2026 18:24:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 22 Apr 2026 18:24:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 22 Apr 2026 18:24:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d11ac9fed97ecbf8481acd5cd9a433e95e4292cf5dfe6e71fafaab6532a25`  
		Last Modified: Wed, 22 Apr 2026 18:26:02 GMT  
		Size: 19.5 MB (19476169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eff4be5d7da60599d44d1988e36bff3f09908653be7b82d4221c2f125bcc808`  
		Last Modified: Wed, 22 Apr 2026 18:26:11 GMT  
		Size: 390.8 MB (390824733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49c5f18c8ad0e1bb87021df4e46eaa6769615d2f35e0861d136801801daa5a9`  
		Last Modified: Wed, 22 Apr 2026 18:26:00 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ff3cae98699bd173854b82d531c153440b0501db4c1936b6f80b2809af150a`  
		Last Modified: Wed, 22 Apr 2026 18:26:02 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68db17eedd597a855197e6bfb018f3945e28d9fd05cc1afb412ebc7fa6889af`  
		Last Modified: Wed, 22 Apr 2026 18:26:02 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78d490bf1bf84766d9dbdec77c019a2c5dbd9f69b741fd5e0b5538fe19f733a`  
		Last Modified: Wed, 22 Apr 2026 18:26:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a4ba4de2fd96112b6e9c6895ef2cd4be095c4d813c2b971c8e4231f3a8604`  
		Last Modified: Wed, 22 Apr 2026 18:26:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2831fd6d2400276737712e1c70df06477bdee81805e4e94c61389e125cb40547`  
		Last Modified: Wed, 22 Apr 2026 18:26:04 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2aca9a0539ef270bc267b974197ece87c0baa361d601b7af18a65004e38616`  
		Last Modified: Wed, 22 Apr 2026 18:26:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7e98de09350a4346c22fbb45b13ee30acfb1baebfb9641b1e317344a00129e`  
		Last Modified: Wed, 22 Apr 2026 18:26:05 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e69a4a21ed7f3cb7a0df98492138d94c8ca87828cc0f034ca119ab80e20118`  
		Last Modified: Wed, 22 Apr 2026 18:26:05 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76935e0f717dc366d4b59c11f9e3eabc92747c8543dc6b10b19b8b67db8959f4`  
		Last Modified: Wed, 22 Apr 2026 18:26:06 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:dbfee7f97c4898d964051a87ce3425dc424575eda16845d0519f3ec5a432801e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5836290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34901e9036a64c617690f479f99239f02981aea8e71f3bd0de0d3f47edb78f77`

```dockerfile
```

-	Layers:
	-	`sha256:564089afd5404f76c73c4bf3f1a68254b93bca02b4d1beaa33f0af796263605f`  
		Last Modified: Wed, 22 Apr 2026 18:26:01 GMT  
		Size: 5.8 MB (5792807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a886a9c5b9c3042c2344ae6ca6b7b2fa40406dfef49cc295d8ff08dbd9de91`  
		Last Modified: Wed, 22 Apr 2026 18:26:00 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
