<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.14`](#kibana81914)
-	[`kibana:9.2.8`](#kibana928)
-	[`kibana:9.3.3`](#kibana933)

## `kibana:8.19.14`

```console
$ docker pull kibana@sha256:aecce3620cdd3e750b93684e9211c9c7a9ccbb80a263fd52cf0f2e37506f12c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.14` - linux; amd64

```console
$ docker pull kibana@sha256:126781b176b5410866475fa651062367db731f423d528c1c93586563aa75eee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.7 MB (444693498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea008c4f0b0909a0880529abbdefed2f09aee1b8e0ead5b8810e02f3a029ab`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 17:12:28 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 08 Apr 2026 17:12:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Apr 2026 17:21:41 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 08 Apr 2026 17:21:41 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:21:41 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 08 Apr 2026 17:21:42 GMT
RUN fc-cache -v # buildkit
# Wed, 08 Apr 2026 17:21:42 GMT
WORKDIR /usr/share/kibana
# Wed, 08 Apr 2026 17:21:42 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 08 Apr 2026 17:21:42 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:21:42 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:21:42 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 08 Apr 2026 17:21:42 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:21:42 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 08 Apr 2026 17:21:43 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 08 Apr 2026 17:21:44 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 08 Apr 2026 17:21:44 GMT
LABEL org.label-schema.build-date=2026-04-02T14:20:50.138Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.14 org.opencontainers.image.created=2026-04-02T14:20:50.138Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f0f7aa44834eefe7c9cee43c8527588e0e952d54 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.14
# Wed, 08 Apr 2026 17:21:44 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 08 Apr 2026 17:21:44 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 08 Apr 2026 17:21:44 GMT
USER 1000
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d1c3d83575e0ffe8e2743091458127162c73a28803b1212b43b2afad9ea4b1`  
		Last Modified: Wed, 08 Apr 2026 17:22:45 GMT  
		Size: 11.8 MB (11836706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd263d2c0857586686099d1e7b9df6ec8fdf1010d385bf0c28722d3b7d30584`  
		Last Modified: Wed, 08 Apr 2026 17:22:52 GMT  
		Size: 386.5 MB (386479339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e619f6c0e3112936aafac52aacef33afd1fd00076f2f78579948d7f300fe22f`  
		Last Modified: Wed, 08 Apr 2026 17:22:43 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0691093b98b2b3fc347ac1925b2723621dbf38ffc6d933dfa6e3bea99696f93`  
		Last Modified: Wed, 08 Apr 2026 17:22:45 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6646ec4c9f076c43c7bf316617438d8fc06fb6f593d1897e3ae759d397b931`  
		Last Modified: Wed, 08 Apr 2026 17:22:45 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab7e978d34ff0bdcb1b647f9775384c6cbeab950517eda07f91c9161f27a623`  
		Last Modified: Wed, 08 Apr 2026 17:22:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6300f54e705269d49d3b5201b3cebd5484910323328832f750d60c3570c0d45`  
		Last Modified: Wed, 08 Apr 2026 17:22:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb342cb0a011254a7bd745e81eff0862c4a4247c7dc128090fe6efdc2d5e9c2`  
		Last Modified: Wed, 08 Apr 2026 17:22:46 GMT  
		Size: 4.8 KB (4819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee93ea7c0b7596db7943ed95ce241e40cfd7be677814991ce534b78c349a900`  
		Last Modified: Wed, 08 Apr 2026 17:22:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5a3be393782d0ec701b6cddfe1c38c58f05ccad5142718e2383d5606b8527`  
		Last Modified: Wed, 08 Apr 2026 17:22:48 GMT  
		Size: 161.7 KB (161742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d6056a8905945fd99daf3e718f49878aa7a274d62da03aa69162b643b3df7a`  
		Last Modified: Wed, 08 Apr 2026 17:22:48 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.14` - unknown; unknown

```console
$ docker pull kibana@sha256:9e243d10717a21004b1d75cfd2ca97cc286a11be3f64aba04450016642a9b5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9231b095def7a5bfe322a23b6d2d22ac3a189acdce213debdfe28521524f8ffd`

```dockerfile
```

-	Layers:
	-	`sha256:a84104269ec623bb00515e76d00ac26cc342215bdd615b6a957c70ceb53acc68`  
		Last Modified: Wed, 08 Apr 2026 17:22:44 GMT  
		Size: 4.9 MB (4931399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1be373c3d79da5da923c31333fc6b93e1be135e7eadebd4685fe46f7433139`  
		Last Modified: Wed, 08 Apr 2026 17:22:44 GMT  
		Size: 40.9 KB (40927 bytes)  
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
$ docker pull kibana@sha256:a287da5c15b043cfdf52f0129d623b163a3ef9d838406f44447865798f08148e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.8` - linux; amd64

```console
$ docker pull kibana@sha256:861c1fe9c13ed2614f6b8bc8e8dd874693818ffe0731c9e9c454d59b1fe70d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447818048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ca65dc96cf149e9fabc44cc2a3b490540a78610aa89c13fdb42ca15cbee142`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:50 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 08 Apr 2026 17:29:50 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:38:30 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 08 Apr 2026 17:38:31 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:38:31 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 08 Apr 2026 17:38:31 GMT
RUN fc-cache -v # buildkit
# Wed, 08 Apr 2026 17:38:31 GMT
WORKDIR /usr/share/kibana
# Wed, 08 Apr 2026 17:38:31 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 08 Apr 2026 17:38:31 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:38:31 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:38:31 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 08 Apr 2026 17:38:31 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:38:32 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 08 Apr 2026 17:38:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 08 Apr 2026 17:38:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 08 Apr 2026 17:38:33 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 08 Apr 2026 17:38:33 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 08 Apr 2026 17:38:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:38:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 08 Apr 2026 17:38:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 08 Apr 2026 17:38:33 GMT
USER 1000
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb318b94732b558538ef11a1af74d80f717b19959c5710ef23a7c83ead1de05`  
		Last Modified: Wed, 08 Apr 2026 17:39:27 GMT  
		Size: 19.5 MB (19521326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82f99f7398e83cf339f8d57f7bfbcb92c52d4fad8decd295228875fbe237239`  
		Last Modified: Wed, 08 Apr 2026 17:39:36 GMT  
		Size: 371.8 MB (371755694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0958765f4dcf509450250752e2a80bdf64341e3fd05daed982d2fa8d11ab13`  
		Last Modified: Wed, 08 Apr 2026 17:39:26 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4870b232c74ea980536e760c6cec26d37a2fae160056453a7d02f5c2e5d005c`  
		Last Modified: Wed, 08 Apr 2026 17:39:27 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fdc47652600f744bea017c411e3ae96d646ec5683fd2afd3278c65084219f9`  
		Last Modified: Wed, 08 Apr 2026 17:39:27 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80f897423f8cbb316480d6fc7213fd07c0b157b987fd57648ddc6ff1e90e205`  
		Last Modified: Wed, 08 Apr 2026 17:39:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe15d1a67f6b594549ca9327e9b0af5a5e7fee74a4aed60e15bb1a6d51743c8e`  
		Last Modified: Wed, 08 Apr 2026 17:39:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8f39fd0f7b40b97ea8eb921ad53e47206e4ba6850508576117311d0450de3`  
		Last Modified: Wed, 08 Apr 2026 17:39:29 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf99cdd67065aa3a81e7355ec46cc647db2ec407bfbadcce93d967d4b6957f40`  
		Last Modified: Wed, 08 Apr 2026 17:39:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fe9b550fbd9b072b4cc86c183704f3049e1375de74b75a376d3396fbc27490`  
		Last Modified: Wed, 08 Apr 2026 17:39:30 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a628560ffbc20af83957fa3f0a73225dd262b784564a49d301a813c17867a14`  
		Last Modified: Wed, 08 Apr 2026 17:39:30 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb9dd101bbbe45338dad2ca48771e4ecfaa1ac650911ca42f9811205afd5f66`  
		Last Modified: Wed, 08 Apr 2026 17:39:32 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:66acdf4bb48144d95c5acabfb039308dc320c0bd966ae246bcf5a6670e03ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff18bd680d47d0ad8c79d95f87183f5130e183e02b42d9b94f04eb52a3cc341`

```dockerfile
```

-	Layers:
	-	`sha256:fae262bae134680840cb61b18cf5dd5e2e698ed8b7d104db96bc2951c2d69b58`  
		Last Modified: Wed, 08 Apr 2026 17:39:27 GMT  
		Size: 5.7 MB (5730200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c6ac942ae966cc46c5fb15f5cd3e657f2f75bf07976094088c6d6528480782`  
		Last Modified: Wed, 08 Apr 2026 17:39:26 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:62fa24b66f7f6771a2099e35e306fc56dd8eed3dc0c15865ee1088f31e6e7380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.7 MB (459729396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a489a5470cdc8abf87c1da57deafeabd3c2f49783dee4524994e6f6729e18c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:28:52 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 08 Apr 2026 17:28:52 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
RUN fc-cache -v # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
WORKDIR /usr/share/kibana
# Wed, 08 Apr 2026 17:36:17 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:36:17 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:36:17 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 08 Apr 2026 17:36:17 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:36:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 08 Apr 2026 17:36:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 08 Apr 2026 17:36:19 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 08 Apr 2026 17:36:19 GMT
LABEL org.label-schema.build-date=2026-04-02T11:37:15.160Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.8 org.opencontainers.image.created=2026-04-02T11:37:15.160Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2484ea8af037aecc848b80cdf39f66b62eb7b5a0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.8
# Wed, 08 Apr 2026 17:36:19 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 08 Apr 2026 17:36:19 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:36:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 08 Apr 2026 17:36:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 08 Apr 2026 17:36:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c08cf98d39cca1c76f02099d5cbf8ab39d76f7687f11dd50203849dfc68f853`  
		Last Modified: Wed, 08 Apr 2026 17:37:24 GMT  
		Size: 19.5 MB (19480476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22619aeaedd25c460e6c698d8e148fb6e8260db425c904e646ad6a25610d8dd`  
		Last Modified: Wed, 08 Apr 2026 17:39:23 GMT  
		Size: 385.5 MB (385491792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bba1ea041a013f21d15f09ccd28e03832d0e33cfa3c17067d9546a787bdad39`  
		Last Modified: Wed, 08 Apr 2026 17:37:23 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58221bc4ea52050a534386628d301ce230e45f28519e44427f590501803a60c`  
		Last Modified: Wed, 08 Apr 2026 17:37:24 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79a7c1f60dbc2439120b683a334984d1cfd254156a3a4594c5b116af2643812`  
		Last Modified: Wed, 08 Apr 2026 17:37:24 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec6ef69f4279622b0da79aacd0964ec331c7aa41d2f4b30ebc584c4c9f2c479`  
		Last Modified: Wed, 08 Apr 2026 17:37:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2832467aab63302899831cf2aaf6cb006e7031c68e45a806f40fcadae77dc901`  
		Last Modified: Wed, 08 Apr 2026 17:37:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed8a7fbd39ea1539039153d1400c6ea977f82afb252c2efc8d3ed78e7b58197`  
		Last Modified: Wed, 08 Apr 2026 17:37:26 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1db181e97e268bf83f23969fd2e7697a9481bbc1ffa312e3817413af018f3e9`  
		Last Modified: Wed, 08 Apr 2026 17:37:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ed15b1314fe2e8ba12d3d8db9d5bab0f1af0b83d3495db817e5514deab101`  
		Last Modified: Wed, 08 Apr 2026 17:37:28 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8544c8550a59f6023fbb81736e194250a9c806dcdce16c4539acfb86948354c6`  
		Last Modified: Wed, 08 Apr 2026 17:37:28 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fff96bebb9f1165ac7f220f9a9c9088303b44169372cae98f622a245b43e49`  
		Last Modified: Wed, 08 Apr 2026 17:37:30 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.8` - unknown; unknown

```console
$ docker pull kibana@sha256:d1145385086ae5f00cd9d95550070130960ddba37390f6fd75addd24ea8cbd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5772355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd18428f286d2798d2fb65002b50ce6e7d65b4afc3e482520e3c5a2e58217e`

```dockerfile
```

-	Layers:
	-	`sha256:3904be75565aa0cef0ef29b42e197952ec406c8e17493a3c4b4411077f14c108`  
		Last Modified: Wed, 08 Apr 2026 17:37:23 GMT  
		Size: 5.7 MB (5728872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31529e9694ee5cdc38aca0d929ed5a7a1b8aac4363055d44d850812f1e972330`  
		Last Modified: Wed, 08 Apr 2026 17:37:23 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.3`

```console
$ docker pull kibana@sha256:89fdff9b0922ff60b9cbc471c34582cc84c282735ea3451231b8c02a54e88275
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.3` - linux; amd64

```console
$ docker pull kibana@sha256:15524431d1c432b614e88565bf74de0ad5b6d49f8703dcaedc8a1ea3577d2d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453148083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619f442db712a0a12b611032d318dabe3a4fde9ec3961ea0cafc67a7f15bca1e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:52:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:52:35 GMT
ENV container oci
# Wed, 08 Apr 2026 04:52:35 GMT
COPY dir:7e1fa46f22db9f15d490572bbe30fedb301ac6c3ea9196eda6f29556472de21e in /      
# Wed, 08 Apr 2026 04:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:52:35 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
COPY file:ae354e2e550b8f696bd3d91d5d8612e98fc2326218cd4fb2f1b9a2c0a34da7b7 in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:52:36 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:52:24Z" "org.opencontainers.image.created"="2026-04-08T04:52:24Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:52:24Z
# Wed, 08 Apr 2026 17:29:23 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 08 Apr 2026 17:29:23 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:38:36 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 08 Apr 2026 17:38:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:38:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 08 Apr 2026 17:38:37 GMT
RUN fc-cache -v # buildkit
# Wed, 08 Apr 2026 17:38:37 GMT
WORKDIR /usr/share/kibana
# Wed, 08 Apr 2026 17:38:37 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 08 Apr 2026 17:38:37 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:38:37 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:38:37 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 08 Apr 2026 17:38:37 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:38:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 08 Apr 2026 17:38:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 08 Apr 2026 17:38:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 08 Apr 2026 17:38:38 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 08 Apr 2026 17:38:38 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 08 Apr 2026 17:38:39 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:38:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 08 Apr 2026 17:38:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 08 Apr 2026 17:38:39 GMT
USER 1000
```

-	Layers:
	-	`sha256:d70a90fdfb362fd73aa4eb84ad1d7bb2a584e2d13f7e6f51200923818455d13e`  
		Last Modified: Wed, 08 Apr 2026 05:42:00 GMT  
		Size: 40.0 MB (39982647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234aec4f137189a56104b9dfddfdfbadad5a5d24705dd67f4b0aafed9467ae8`  
		Last Modified: Wed, 08 Apr 2026 17:39:38 GMT  
		Size: 19.5 MB (19521247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527f6b5b0e01e31bad19fba4945353c1c3a206b7e0d4d8a768aa5295ddd25fd6`  
		Last Modified: Wed, 08 Apr 2026 17:39:47 GMT  
		Size: 377.1 MB (377085786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a049f24f7cebb553d5240b1485fb5aeae1cce7ee012d0caddef25bb7d6d55d9`  
		Last Modified: Wed, 08 Apr 2026 17:39:36 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90f0a4d21317fb93b2f196d9e7e897d3a54ff230850eac7a6bd1da4f001a76a`  
		Last Modified: Wed, 08 Apr 2026 17:39:38 GMT  
		Size: 16.5 MB (16460482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2e5cf1d7b4376d64d9be768a8f0654211dfc11a767f962b001df77f9d16c2e`  
		Last Modified: Wed, 08 Apr 2026 17:39:38 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc7e867f4848190bb58218457cc9b6e44b74715667dfb3f11342d24cb215a51`  
		Last Modified: Wed, 08 Apr 2026 17:39:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac58c162494589ff7401611f7c9d0f48410aa3de4741bacbb60eee9da2496c4`  
		Last Modified: Wed, 08 Apr 2026 17:39:39 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17dd7bbb7449ece362dd507d8e652e78a5fc18321beba84eda9e65168743a79`  
		Last Modified: Wed, 08 Apr 2026 17:39:40 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a70b88b197d7887a6b89156eb6c23f138afbf9ae32b8c450a7e3e5a258e83`  
		Last Modified: Wed, 08 Apr 2026 17:39:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a04d22bdc539f2706b6e00ad30e3824f96b9ed7ba1780f6ecc76ecdeb45a20`  
		Last Modified: Wed, 08 Apr 2026 17:39:41 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044d23b6004aba1349c48d294a6559fadc49dde77b3a4606ea5e0b9b23a0305d`  
		Last Modified: Wed, 08 Apr 2026 17:39:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97492fbba0a7f1e154a9fb5cd039fb2b44d15a9614c0a70eb218897300d26516`  
		Last Modified: Wed, 08 Apr 2026 17:39:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:1ebfd65cfc0cad1af2f018e2ac28ce1119d8edd32b8cece0a9e72d3d6126ab1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5837345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaf30cd231834adb5247d31e52425d51cf0ccb358c3d8436856a92e68399514`

```dockerfile
```

-	Layers:
	-	`sha256:eff9b495740764403554d9f8bfb489e620917d70c85ad4b5dfd948f9ec67b709`  
		Last Modified: Wed, 08 Apr 2026 17:39:37 GMT  
		Size: 5.8 MB (5794119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee031e57d720a85871503e520e726a3357abd347c4c979296696cccd9a71cbc3`  
		Last Modified: Wed, 08 Apr 2026 17:39:36 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:abdca6b1b924bce894247c53f9f954715a86cf80679c5b4e21fffaa166bedd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.1 MB (465063620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bf5d56a66dddf326b32464b8c4d63296052b87b682bf8c4f11fed7560166af`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.expose-services=""
# Wed, 08 Apr 2026 04:55:31 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 08 Apr 2026 04:55:31 GMT
ENV container oci
# Wed, 08 Apr 2026 04:55:32 GMT
COPY dir:e3968b666ccf8b1da827a1f934e7d66b38ad6335b0bf20a2a01583a6f9f3fdaa in /      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 08 Apr 2026 04:55:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /usr/share/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:32 GMT
COPY file:696dd319730ed197429cabc840fe5bc51d4286962e2bde67f5d48480e8cbdd7b in /root/buildinfo/labels.json      
# Wed, 08 Apr 2026 04:55:33 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="470b852dce8e880416927445bd12327938b329e2" "org.opencontainers.image.revision"="470b852dce8e880416927445bd12327938b329e2" "build-date"="2026-04-08T04:55:18Z" "org.opencontainers.image.created"="2026-04-08T04:55:18Z" "release"="1775623882"org.opencontainers.image.revision=470b852dce8e880416927445bd12327938b329e2,org.opencontainers.image.created=2026-04-08T04:55:18Z
# Wed, 08 Apr 2026 17:28:52 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 08 Apr 2026 17:28:52 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:36:31 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 08 Apr 2026 17:36:31 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 08 Apr 2026 17:36:31 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 08 Apr 2026 17:36:32 GMT
RUN fc-cache -v # buildkit
# Wed, 08 Apr 2026 17:36:32 GMT
WORKDIR /usr/share/kibana
# Wed, 08 Apr 2026 17:36:32 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 08 Apr 2026 17:36:32 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 08 Apr 2026 17:36:32 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:36:32 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 08 Apr 2026 17:36:32 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 08 Apr 2026 17:36:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 08 Apr 2026 17:36:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 08 Apr 2026 17:36:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 08 Apr 2026 17:36:34 GMT
LABEL org.label-schema.build-date=2026-04-01T20:36:21.616Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bf7be757e102e9c064ff7161919d283963c7d93d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.3 org.opencontainers.image.created=2026-04-01T20:36:21.616Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bf7be757e102e9c064ff7161919d283963c7d93d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.3
# Wed, 08 Apr 2026 17:36:34 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 08 Apr 2026 17:36:34 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 08 Apr 2026 17:36:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 08 Apr 2026 17:36:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 08 Apr 2026 17:36:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:1ffb0d1826b0600c6d4836c7ada23756af4c1475452e12ce1bed713d58738262`  
		Last Modified: Wed, 08 Apr 2026 05:41:58 GMT  
		Size: 38.2 MB (38200278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d668e74ccfd9ea5f3b43bf824145c3888c0697358e207cf57ab897a755ccdfe`  
		Last Modified: Wed, 08 Apr 2026 17:37:39 GMT  
		Size: 19.5 MB (19480671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300120b2a62e14c0d3744ac1935735bd702cf52e62e66daf15bd7e2b192d2561`  
		Last Modified: Wed, 08 Apr 2026 17:37:48 GMT  
		Size: 390.8 MB (390825800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c5671bc8728b8887d8c168a4c1aa59ebdda1276151d4d17fcaa02e5105c676`  
		Last Modified: Wed, 08 Apr 2026 17:37:38 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220856bb2cd823e374aaa9a9c7abb403f8fd09a57da93379bb2e7dfe764021ca`  
		Last Modified: Wed, 08 Apr 2026 17:37:39 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cf3997d7e885cdeb3355e579581707ad603ac2cc720600239a43f4f678363f`  
		Last Modified: Wed, 08 Apr 2026 17:37:39 GMT  
		Size: 5.2 KB (5218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96546e929b64c7c83838360b700ac927a8cd3b41d664ebb564780ac393f6fc7`  
		Last Modified: Wed, 08 Apr 2026 17:37:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f639a11184cac5f7587bc6bd5950de6e2b68c823f5ea131e730b5b7e82be61`  
		Last Modified: Wed, 08 Apr 2026 17:37:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c7a1665d56ce44b316ae372ddc4032ef423617bf621701d13cbb098d1fd5f5`  
		Last Modified: Wed, 08 Apr 2026 17:37:41 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e92549ba2261bf78d98aac499b0bbf06f9a9e8b3a9b62514fc4c5980237b3d`  
		Last Modified: Wed, 08 Apr 2026 17:37:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb069daa20195f9fb14170877637ea14b85adf198bba21034912527448b209b5`  
		Last Modified: Wed, 08 Apr 2026 17:37:42 GMT  
		Size: 73.4 KB (73447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5db45ac7eb12b1bc25c22b193e3d7c6c9930e4e3a1fe4c69975aaf57c3618f`  
		Last Modified: Wed, 08 Apr 2026 17:37:43 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083f4600a74aea7eb8dadb1feeb9559535faaa23dc165b3d0bee4a972184d31d`  
		Last Modified: Wed, 08 Apr 2026 17:37:44 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.3` - unknown; unknown

```console
$ docker pull kibana@sha256:f987b114a04cbaaef23f68482bf61565f7b97154967c21fa93dcdd2650d5a810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5836273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218a6c5c33b20ffd7275d239ad6b6b2a0345a623abf17001c34f2877c6af902e`

```dockerfile
```

-	Layers:
	-	`sha256:2142eb2cdaf69ddcf3494d21e0d91690efe74ff9379b7ba564ca79ada47a1854`  
		Last Modified: Wed, 08 Apr 2026 17:37:38 GMT  
		Size: 5.8 MB (5792791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:951819dea96a667ab1ac26a76b946d11bf1544f54ce805c693009171b50c2c76`  
		Last Modified: Wed, 08 Apr 2026 17:37:38 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json
