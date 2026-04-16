<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.14`](#kibana81914)
-	[`kibana:9.2.8`](#kibana928)
-	[`kibana:9.3.3`](#kibana933)

## `kibana:8.19.14`

```console
$ docker pull kibana@sha256:b7645a86a6c6c2c8cd81ac9b676b6d3d2d81cdccd4099be0bc1d6b87ebe8cc04
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
$ docker pull kibana@sha256:27203c03752f7d01db97813146984df12c49c08cb58c13a312bcd64bd6c1a4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.4 MB (457406856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dc9aecf3ec0d9b97388e83f0319cd518f2699be4041f206b52e0f0ee010683`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 17:10:29 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 08 Apr 2026 17:10:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 17:17:38 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 08 Apr 2026 17:17:39 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:17:39 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 08 Apr 2026 17:17:39 GMT
RUN fc-cache -v # buildkit
# Wed, 08 Apr 2026 17:17:39 GMT
WORKDIR /usr/share/kibana
# Wed, 08 Apr 2026 17:17:39 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 08 Apr 2026 17:17:39 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:17:39 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:17:39 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 08 Apr 2026 17:17:39 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:17:40 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 08 Apr 2026 17:17:41 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 08 Apr 2026 17:17:41 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 08 Apr 2026 17:17:41 GMT
LABEL org.label-schema.build-date=2026-04-02T14:20:50.138Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T14:20:50.138Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 08 Apr 2026 17:17:41 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 08 Apr 2026 17:17:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 08 Apr 2026 17:17:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e19ab959cb1c4c6c3c08be72bee79a286d626957b511e6b64fb3e70a4a4d9f0`  
		Last Modified: Wed, 08 Apr 2026 17:18:46 GMT  
		Size: 11.7 MB (11670789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af49345f97d3a04bd90684f5fee5fc72d2b5c9377e0e957affb96837dd7669b`  
		Last Modified: Wed, 08 Apr 2026 17:18:54 GMT  
		Size: 400.2 MB (400221908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ffb99273a7ced09e063a0e6e328e87ec819f74ac430ab1a0d74c4d02e898f6`  
		Last Modified: Wed, 08 Apr 2026 17:18:45 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708fa10b3aca2faf16816db714b115f727639ac8e4544271ea422f57d77e8e67`  
		Last Modified: Wed, 08 Apr 2026 17:18:46 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d863bfaf21434dabe9ee50b677aa13845e55577b6dc662743795949dea4e80`  
		Last Modified: Wed, 08 Apr 2026 17:18:47 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb547ff58866fdb5f8144b5f6f17cab1dca6176303a61d37f1d25ac07e0323fb`  
		Last Modified: Wed, 08 Apr 2026 17:18:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b94a1919acc78393e3a1c791c5d131044c4234649fe117b7e7eaf975171a56`  
		Last Modified: Wed, 08 Apr 2026 17:18:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfcfece2dfda3d3cc8e542c0107929b8352a90ea2f44ff57b49d189d166e771`  
		Last Modified: Wed, 08 Apr 2026 17:18:48 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d687cbfed33204d470f61abcf0d1bb34a6e5c1f92bae7ffabbf5dc39baa21d8`  
		Last Modified: Wed, 08 Apr 2026 17:18:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83feb4bd05b411d0b5eb143ce248c6f76fe8bd0cd9eee33284c9c12639cd82c`  
		Last Modified: Wed, 08 Apr 2026 17:18:50 GMT  
		Size: 158.3 KB (158258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e047433646d0d9a85ff65b1d0a6d31a099fb1a869a452957d5dd5abf5f7753`  
		Last Modified: Wed, 08 Apr 2026 17:18:49 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.14` - unknown; unknown

```console
$ docker pull kibana@sha256:f5ad924710fe0b1ecf2ef79e1e13bacad83017d5bf741a48d8199c9619c9d3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e8602f6a94f176782775292f789370433ec6fa57866295a68d2630bbf54bd9`

```dockerfile
```

-	Layers:
	-	`sha256:118b3ccf3283b05ae8a1b61c13b8f116fbff8c43c95c6ccb1819ea3eb1651ee4`  
		Last Modified: Wed, 08 Apr 2026 17:18:46 GMT  
		Size: 4.9 MB (4932463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765599ad145db98b19f51644d4b55fe9fa7ed3cdcc9221b0a500395561292868`  
		Last Modified: Wed, 08 Apr 2026 17:18:45 GMT  
		Size: 41.2 KB (41175 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.8`

```console
$ docker pull kibana@sha256:d19e8808ab0d7d9b3dc5b93b47cfdff26fc9da0f50c227f7450d1e9686e2a8c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.8` - linux; amd64

```console
$ docker pull kibana@sha256:a6bc474c7bf2b200b419970dffa296624b02c6c52ebc4b9ee0ade4a2a8210cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.9 MB (447859162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7126cde6935a8bbf690f0ae67a1d9fbba7c5c7742888ac32813af46f4029573`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 14 Apr 2026 20:46:15 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 14 Apr 2026 20:46:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:55:30 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 14 Apr 2026 20:55:30 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:55:30 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 14 Apr 2026 20:55:30 GMT
RUN fc-cache -v # buildkit
# Tue, 14 Apr 2026 20:55:30 GMT
WORKDIR /usr/share/kibana
# Tue, 14 Apr 2026 20:55:31 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 14 Apr 2026 20:55:31 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:55:31 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:55:31 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 14 Apr 2026 20:55:31 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:55:31 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 14 Apr 2026 20:55:32 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 14 Apr 2026 20:55:32 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 14 Apr 2026 20:55:32 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Tue, 14 Apr 2026 20:55:32 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 14 Apr 2026 20:55:32 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:55:32 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 14 Apr 2026 20:55:32 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 14 Apr 2026 20:55:32 GMT
USER 1000
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb891d926617908c8b3312f69010fa56ab70553c820a913c3f4269635b24eaa`  
		Last Modified: Tue, 14 Apr 2026 20:56:29 GMT  
		Size: 19.5 MB (19520039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba1332fdce13ae186b9ce37b43eb3d21509fdd09efae1fc3508eef43c0be9d1`  
		Last Modified: Tue, 14 Apr 2026 20:56:36 GMT  
		Size: 371.8 MB (371764184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08081d56f38107bd6ddbe1c9fe865fbc8ddbc03614abadf745d9a1a6c5307d9a`  
		Last Modified: Tue, 14 Apr 2026 20:56:28 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbce9401d42001b2922af562e425fba498522d6373379acb49f70e41f3acd35f`  
		Last Modified: Tue, 14 Apr 2026 20:56:29 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec4702b534e880af377b7fb96bbc1155d972e1a53e0772970115624f7bd2b3a`  
		Last Modified: Tue, 14 Apr 2026 20:56:29 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cefa3b5393068a40b12c4aeb28f3544d3d06e15447aefd44fb0bf2a4ce7c3df`  
		Last Modified: Tue, 14 Apr 2026 20:56:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d124272c08743a4b58b1dd360f507038b06f624a17f7f12952c4768a6e02f6`  
		Last Modified: Tue, 14 Apr 2026 20:56:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae59b7fd740411577612cc71617a8162a4c7a2f63e57751f78e63d6f1570155`  
		Last Modified: Tue, 14 Apr 2026 20:56:31 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c19b49693a1a52dc3088e0821e95f5ac57d1805ff06883f9c81495de62b953`  
		Last Modified: Tue, 14 Apr 2026 20:56:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dc23a9a38b8da66d497932cde257cf80aefb125f55ed77083b82751ee06a16`  
		Last Modified: Tue, 14 Apr 2026 20:56:32 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e28dd0f8f51884422c89d372a836170b4783f65c4aca0e1f9385e24bc12922`  
		Last Modified: Tue, 14 Apr 2026 20:56:32 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f69988d1913fde644e329d18194cb1198221fc6b3f26052f2a64a5a412d533`  
		Last Modified: Tue, 14 Apr 2026 20:56:33 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:5be49a55cf9ee042caf3fcedce8df2bad6c42235557a744fb6fa3f6216d94aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c183f5b22704c116afea7e99f431c169929b9f21499141eeab8d6d6dabf42c46`

```dockerfile
```

-	Layers:
	-	`sha256:340d7fa02bb0aee4e3b2776f37c8646151dee24369e20082a5973fa91aac1dfc`  
		Last Modified: Tue, 14 Apr 2026 20:56:28 GMT  
		Size: 5.7 MB (5730216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e65b0f024d45905f26b430d8fac9d01e39e0146ca5dda04c0dc9086178d9f7`  
		Last Modified: Tue, 14 Apr 2026 20:56:28 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:c205eaf3ff57b101813c7ae18493f0de00f0177800fb3eda54f84a174f4169d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.7 MB (459725815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a0ba36bba79c7c7ff23e36fa4597171608e1829473029a1fb34a40f02f6baa`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 14 Apr 2026 20:45:38 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 14 Apr 2026 20:45:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:53:02 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 14 Apr 2026 20:53:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:53:03 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 14 Apr 2026 20:53:03 GMT
RUN fc-cache -v # buildkit
# Tue, 14 Apr 2026 20:53:03 GMT
WORKDIR /usr/share/kibana
# Tue, 14 Apr 2026 20:53:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 14 Apr 2026 20:53:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:53:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:53:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 14 Apr 2026 20:53:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:53:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 14 Apr 2026 20:53:05 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 14 Apr 2026 20:53:05 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 14 Apr 2026 20:53:05 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Tue, 14 Apr 2026 20:53:05 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 14 Apr 2026 20:53:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:53:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 14 Apr 2026 20:53:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 14 Apr 2026 20:53:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eda27e52fe6929f8035ac0ec51374dd8bf2a4a1d02b2758165ba3da6d04de68`  
		Last Modified: Tue, 14 Apr 2026 20:54:10 GMT  
		Size: 19.5 MB (19475787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2eaea39be293553628a0c0ef4211905ef51c1e76af8fc02c8fab2595713b81`  
		Last Modified: Tue, 14 Apr 2026 20:54:17 GMT  
		Size: 385.5 MB (385493065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757849fb99562a1ded5e069c1a31837bb7bff3ef152fbe46ffa0ebd5c423346b`  
		Last Modified: Tue, 14 Apr 2026 20:54:09 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7647e3fb6fdd36de3d7263688720ac44ded1dd486de708960e25e0d6f9b637`  
		Last Modified: Tue, 14 Apr 2026 20:54:09 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4088255c2646297ca3aefc06488f35b88b385aa2cca49e1686d07c0722250fb`  
		Last Modified: Tue, 14 Apr 2026 20:54:10 GMT  
		Size: 5.2 KB (5219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9643ba4b13010b53c1c40e3f18ed69fb4abf67db7b897d60ebee7e7f45316822`  
		Last Modified: Tue, 14 Apr 2026 20:54:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97523be9ee7fdc6757498677b3402d69bc9bcc80072073940b26c2bc1ea5576d`  
		Last Modified: Tue, 14 Apr 2026 20:54:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c776d99f5bca298f7cac6a6b944dda1613232baa09bbe6997228cd4529506528`  
		Last Modified: Tue, 14 Apr 2026 20:54:11 GMT  
		Size: 4.9 KB (4891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3270768094bc428e5ff7615be0972fc238518294d3a878df76d6ae76af15842`  
		Last Modified: Tue, 14 Apr 2026 20:54:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f00637b9c6db75b3b8e98438c1165a8ab16869521d7f4acc3de29821703870`  
		Last Modified: Tue, 14 Apr 2026 20:54:13 GMT  
		Size: 73.4 KB (73444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a444705d82d13ab36d3e9402d6110208f560d1eb9bf74471650a346309d9659`  
		Last Modified: Tue, 14 Apr 2026 20:54:12 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373e44bbd3e363b9db9367f548e1b06221c8b5539591db5f55bfbfc8ba3e6ed2`  
		Last Modified: Tue, 14 Apr 2026 20:54:14 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:88ee8a837dd910f7268bc63af6041f2437c777ec8babab5cb5e1d353f8372c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c8ea2a38f7f126391dc5460c0bbb258f468ad21c7dcc2021190c8f2f662743`

```dockerfile
```

-	Layers:
	-	`sha256:8f369d40eff64da944bae5135718189e42291eb767dc1e6b69431b304c4250d6`  
		Last Modified: Tue, 14 Apr 2026 20:54:09 GMT  
		Size: 5.7 MB (5728888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b9bb25fdeb71d27714e68bb7b721e32e09b96506ed171ddcc68db9561e978`  
		Last Modified: Tue, 14 Apr 2026 20:54:09 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.3`

```console
$ docker pull kibana@sha256:6318ce3634c1cc34e318903ff91b144d5e15e9499d9b97fd7261556320f129d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.3` - linux; amd64

```console
$ docker pull kibana@sha256:3841f7dfd789ec0d1d17bde15df54b09d0945a15fee9ff90faa319046fe881a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453178685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47bc8b24ef9c3cdc50de93580895612ae12ea2970d79ecd4f1c05c35730390bd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 14 Apr 2026 20:46:20 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 14 Apr 2026 20:46:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:56:02 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 14 Apr 2026 20:56:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:56:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 14 Apr 2026 20:56:04 GMT
RUN fc-cache -v # buildkit
# Tue, 14 Apr 2026 20:56:04 GMT
WORKDIR /usr/share/kibana
# Tue, 14 Apr 2026 20:56:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 14 Apr 2026 20:56:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:56:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:56:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 14 Apr 2026 20:56:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:56:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 14 Apr 2026 20:56:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 14 Apr 2026 20:56:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 14 Apr 2026 20:56:06 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Tue, 14 Apr 2026 20:56:06 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 14 Apr 2026 20:56:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:56:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 14 Apr 2026 20:56:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 14 Apr 2026 20:56:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8d2cbbe826c8a6fdb514275d2b93bda587eba6a229c078355cb5d8343665fd`  
		Last Modified: Tue, 14 Apr 2026 20:57:08 GMT  
		Size: 19.5 MB (19520058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbfdeaf865de8154fffa9423ecb3aff28519c50861dd46ea8960ae608ec501b`  
		Last Modified: Tue, 14 Apr 2026 20:57:20 GMT  
		Size: 377.1 MB (377083650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7afc0215d094ae4561daca10c5d8edb12e4cc1fe51ecee2d268b058db18f828`  
		Last Modified: Tue, 14 Apr 2026 20:57:07 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee99cd7fe1753b3f2064e2115496f5ec24fdbff4131aeea60ace386ab7addc1`  
		Last Modified: Tue, 14 Apr 2026 20:57:08 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9729b7f84af6f35e8bafaab0f69ab2b363d5c094545a7f47e13f019e164272`  
		Last Modified: Tue, 14 Apr 2026 20:57:08 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a302ff5f38e184000ed0c2a87bda38ed8e4f1df1c0a85c6bea46887f3cdd77`  
		Last Modified: Tue, 14 Apr 2026 20:57:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babcca8e7022fde4a6b23611ff69a6244770c2dfe1224375639dc61fa0fe0e08`  
		Last Modified: Tue, 14 Apr 2026 20:57:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68eee148ea545b1dba7a66438c51cc07fa7972d08b1a90006f8065da377b190`  
		Last Modified: Tue, 14 Apr 2026 20:57:10 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5776e64656d0ce8e1775979cdb2a51aa8362fcb7b54b36dab79f3a9343f4cfe`  
		Last Modified: Tue, 14 Apr 2026 20:57:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaadf2678a498e4e16b75a76412f395b5078a0cea71a3654b6c2d138662baa8`  
		Last Modified: Tue, 14 Apr 2026 20:57:11 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8670193dcd4b89c82a8e10fc059b55492c7a54cbbcc2ad41a7b57bc1b296a20`  
		Last Modified: Tue, 14 Apr 2026 20:57:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0556d3e5d71b9615ddf57ab0b4295001dda26721809cefc0475cdfc046e8d4bb`  
		Last Modified: Tue, 14 Apr 2026 20:57:12 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:ae237c19a3a33b2bee24769df44024082cbaaa5bd5d53f48399b6b40f53865a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9df231b72a3dcc1dab7d5b07a05af08d614682ae27c4d042b67cab274652a4`

```dockerfile
```

-	Layers:
	-	`sha256:7bdf1296be0be7348256ff7c3a67cde1be2653329ab8753fff8077cbbc499440`  
		Last Modified: Tue, 14 Apr 2026 20:57:07 GMT  
		Size: 5.8 MB (5794135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b9beb6315b2a77cc807ee8eec1b71aec40e171e1b69136bbfd3a83613b264e5`  
		Last Modified: Tue, 14 Apr 2026 20:57:07 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:42e90dc99be1821565e896cc9e13e4ef7ce24dbd2eb9ba4cf609ffed91cd6471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.1 MB (465051660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000123444a54643615553d7df2efdf6b4d05d9f6d2f05c4270803b69d512d59`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
# Tue, 14 Apr 2026 20:45:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 14 Apr 2026 20:45:54 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:53:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 14 Apr 2026 20:53:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 14 Apr 2026 20:53:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 14 Apr 2026 20:53:34 GMT
RUN fc-cache -v # buildkit
# Tue, 14 Apr 2026 20:53:34 GMT
WORKDIR /usr/share/kibana
# Tue, 14 Apr 2026 20:53:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 14 Apr 2026 20:53:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Apr 2026 20:53:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:53:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 14 Apr 2026 20:53:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 14 Apr 2026 20:53:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 14 Apr 2026 20:53:36 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 14 Apr 2026 20:53:36 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 14 Apr 2026 20:53:36 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Tue, 14 Apr 2026 20:53:36 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 14 Apr 2026 20:53:37 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 14 Apr 2026 20:53:37 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 14 Apr 2026 20:53:37 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 14 Apr 2026 20:53:37 GMT
USER 1000
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40417323dde50bf65ab77de25fcc9ad1008bb050a745211b203cb79515018aa8`  
		Last Modified: Tue, 14 Apr 2026 20:54:41 GMT  
		Size: 19.5 MB (19475665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9240e067d05e18b5f48ba358cc3989aced24d9f3b51b858a3945bdc90c058878`  
		Last Modified: Tue, 14 Apr 2026 20:54:48 GMT  
		Size: 390.8 MB (390819007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126f9b9f4d4fad1cd8ca7fc783d97985d2a3f7f255f613a3c342e825c6c1da2b`  
		Last Modified: Tue, 14 Apr 2026 20:54:40 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6c8a7ccaac2d6e443ebf36c0a1c15677948f1c54d528822bf61cf4d689984a`  
		Last Modified: Tue, 14 Apr 2026 20:54:41 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd34882fede23b69b0555b96e5ededf90f4b3f0de2dd5ee13772261f0f374c48`  
		Last Modified: Tue, 14 Apr 2026 20:54:41 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ea99073def1f1f9ffe4b575536c43162f2bc513a9275ed987166fbfe1726dc`  
		Last Modified: Tue, 14 Apr 2026 20:54:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b99292fb9deeb7676c0282820b9040d514736dc14428e50c64d53ea34e621c0`  
		Last Modified: Tue, 14 Apr 2026 20:54:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb221f8dd188f4cbd40c9652314e75acd6e7d8a28046103ab9b4d0192884dac`  
		Last Modified: Tue, 14 Apr 2026 20:54:43 GMT  
		Size: 4.9 KB (4914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149e2b14785e48ce62f078a8a7cfd650144db9338c956a005e09ca9a1d6ef1a`  
		Last Modified: Tue, 14 Apr 2026 20:54:44 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0294325b3db9138588ea90f79205341c71e744dd177bd386386b8940d7bca6f1`  
		Last Modified: Tue, 14 Apr 2026 20:54:44 GMT  
		Size: 73.4 KB (73446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5334000fae807e925ccd44250611fa5c25de477729bc2c59f71022c77d1199e4`  
		Last Modified: Tue, 14 Apr 2026 20:54:44 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4f00e51d3ceb8e978c36a0c6051b2c21ff3cf04e9859cb6c60fc15189b243`  
		Last Modified: Tue, 14 Apr 2026 20:54:45 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:6173f692b5378089d33bcb487632183ff5abce1d69a96a2add55a41f90f05b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5836290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c222c853c6efa1b42da69b206e908e73c26d2e4d05db1c639cf1958e658856d`

```dockerfile
```

-	Layers:
	-	`sha256:732b02137aec842a61c01b19ca164734aa4773da2cbe55e2c1c33cb2b4096301`  
		Last Modified: Tue, 14 Apr 2026 20:54:41 GMT  
		Size: 5.8 MB (5792807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bafdbc2ce3bc9074c40d25e8cad65e5fef858084051f92f382173bbb5c90017d`  
		Last Modified: Tue, 14 Apr 2026 20:54:40 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
