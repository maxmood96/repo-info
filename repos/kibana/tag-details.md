<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.16`](#kibana81916)
-	[`kibana:9.3.5`](#kibana935)
-	[`kibana:9.4.2`](#kibana942)

## `kibana:8.19.16`

```console
$ docker pull kibana@sha256:88844108397f3f1c0049a01216789eb2e03e6da102fd286f0b77f91affa7528b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.16` - linux; amd64

```console
$ docker pull kibana@sha256:348a1283f0e53a49e0eaf733eb39bebdc4f28112d13642be75d07ac671d0b1af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.6 MB (455584151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff2fb5fe709fba889c556d096d46764b997c704abaf4ac80b2336996f67ea94`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:45 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Jun 2026 08:18:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:27:28 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Jun 2026 08:27:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 08:27:29 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Jun 2026 08:27:29 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Jun 2026 08:27:29 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Jun 2026 08:27:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Jun 2026 08:27:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 08:27:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:27:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Jun 2026 08:27:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:27:30 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Jun 2026 08:27:31 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Jun 2026 08:27:31 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Jun 2026 08:27:31 GMT
LABEL org.label-schema.build-date=2026-05-25T11:13:36.011Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T11:13:36.011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Tue, 02 Jun 2026 08:27:31 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Jun 2026 08:27:31 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Jun 2026 08:27:31 GMT
USER 1000
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28362ae3eab75b654312fce59350039748f2679e66ef89457a02250044aaeb53`  
		Last Modified: Tue, 02 Jun 2026 08:28:30 GMT  
		Size: 9.4 MB (9435957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e015babbf11e0b8e73b97c05cb071337d8037ea57619bec1e7370db795eea60`  
		Last Modified: Tue, 02 Jun 2026 08:28:38 GMT  
		Size: 399.8 MB (399771381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b382a5b9c9d7ee92d534c4ecd44082cdb143848d0b3ac010d72e29738d7369`  
		Last Modified: Tue, 02 Jun 2026 08:28:29 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f02f6979b224fefe4ce4522fce43716aaa7ee753ad88fcc2f65ac7ed91c14c`  
		Last Modified: Tue, 02 Jun 2026 08:28:30 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9c7ed1c854fea2cba7d1f5b62772dd2b0aff8c16c932a5969db6a64a88d730`  
		Last Modified: Tue, 02 Jun 2026 08:28:30 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae00fd25b070649c4aabbb9691e901e9e46231fc019a9ed1b5e9a92cba95d87`  
		Last Modified: Tue, 02 Jun 2026 08:28:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e00a11b4e21fb825cc8e6c0b06d89b88bc333651a39a950f756789a222db1d`  
		Last Modified: Tue, 02 Jun 2026 08:28:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9790320220c223f1943c34699dd652cd6f62a602384e26e0fc62b7c608915567`  
		Last Modified: Tue, 02 Jun 2026 08:28:32 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57875b39b4032eeb3b5a271ecbd5b9d653a574a08fb43d2348fc433141de2866`  
		Last Modified: Tue, 02 Jun 2026 08:28:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eeb1390b74a820d32b903c032c16df56f5be3fa12812f445a64291cc528800`  
		Last Modified: Tue, 02 Jun 2026 08:28:33 GMT  
		Size: 161.7 KB (161745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e3945abfd6e2faa9f04a006babbe045fb7499164239f2cf03b61d7233fb61b`  
		Last Modified: Tue, 02 Jun 2026 08:28:33 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.16` - unknown; unknown

```console
$ docker pull kibana@sha256:04628575fa89bdc6d8090746abae78ee2f2f2955c212a9f6da2d364c090e24d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512050edecec276de92f4db0ffbf29e933c3d37123e3988d95dc4dd7eca035fd`

```dockerfile
```

-	Layers:
	-	`sha256:c5c5310838fbf86fa6911494f6de604d73d57b1dd746a5765512929b8a692342`  
		Last Modified: Tue, 02 Jun 2026 08:28:29 GMT  
		Size: 5.0 MB (5029681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0203cb6186db608962d462c5972a1da0ef7d35e7fca3e2f6294a5a35eb3550c7`  
		Last Modified: Tue, 02 Jun 2026 08:28:29 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.16` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9e739b2f26f29f621b7893b5392a9dd3c9367fbfec03dc2db5e97edfd11d7bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467494389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2055baa369fa699b7f1914044a79b96bd6aad0816ea30fdbd4900bb95e72936`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:56 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Jun 2026 08:18:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:26:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Jun 2026 08:26:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 08:26:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Jun 2026 08:26:13 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Jun 2026 08:26:13 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Jun 2026 08:26:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Jun 2026 08:26:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 08:26:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 08:26:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Jun 2026 08:26:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:26:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Jun 2026 08:26:15 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Jun 2026 08:26:16 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Jun 2026 08:26:16 GMT
LABEL org.label-schema.build-date=2026-05-25T11:13:36.011Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T11:13:36.011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Tue, 02 Jun 2026 08:26:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Jun 2026 08:26:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Jun 2026 08:26:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57999fd8820923291c3bea4035b1cd8901f4d1070ebe9a7f0d75e94ca1d878df`  
		Last Modified: Tue, 02 Jun 2026 08:27:25 GMT  
		Size: 9.5 MB (9455724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf5e5ed9eded1f6736bc2fbbe0d89995a90f13e77cad61b52526b3ba846cfdc`  
		Last Modified: Tue, 02 Jun 2026 08:27:35 GMT  
		Size: 412.5 MB (412522163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef3dd8e09fc87102393444fca54717563e4c1efe906359a8bedd51c3f0e6174`  
		Last Modified: Tue, 02 Jun 2026 08:27:25 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9a62598797e75a4f4620ef01c1466b05c8f678fb9a09c4646172ee8bfe5dcc`  
		Last Modified: Tue, 02 Jun 2026 08:27:26 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f570993a8f5eef4e8e6b9e9551dc8a61de251e98484b3bd7b3696ebe93d70755`  
		Last Modified: Tue, 02 Jun 2026 08:27:26 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebef4ad63c06faabb1cf1ba06e0f5e293987a81c767353ebd2014c5c27c97ca`  
		Last Modified: Tue, 02 Jun 2026 08:27:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b26c063d12cc90a7d3f54212059e663bfa8f08795ad9085bd4d01c1a0af0dc4`  
		Last Modified: Tue, 02 Jun 2026 08:27:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58614ff92ae43c6d02226e3dda82eaacdb3f716ad259eb616da47c8ef74e51f`  
		Last Modified: Tue, 02 Jun 2026 08:27:27 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da871c11cc5addd212274eadd2664dba5ec30307b32bcc6880b9de60fd7201aa`  
		Last Modified: Tue, 02 Jun 2026 08:27:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a736e58cfff2879dfa4e7d2e9c396f8f4ce41d10385c428fc34f5881fbfdf87`  
		Last Modified: Tue, 02 Jun 2026 08:27:29 GMT  
		Size: 158.3 KB (158261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95a878a0bd4f35bbc316fff2f7ed84d2a7cfdd04dbf0d02183e8d020a48ae6c`  
		Last Modified: Tue, 02 Jun 2026 08:27:29 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.16` - unknown; unknown

```console
$ docker pull kibana@sha256:5d44fba0b240b26650003d2861fc3e987ab0aae1116787cdead20cdcc3d7320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59063fb082582b9c59f675b36f5b75438ebc9f33af407bf7859bb03948440fa7`

```dockerfile
```

-	Layers:
	-	`sha256:0c63a2c0ab439c5ff2829255ab28ce13ffeee0275a753f00a234f161018a25ea`  
		Last Modified: Tue, 02 Jun 2026 08:27:25 GMT  
		Size: 5.0 MB (5030745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b710b6563e6c1fd77720a9118dfc361760eb76720498b1d9e234e3a88ec9483`  
		Last Modified: Tue, 02 Jun 2026 08:27:24 GMT  
		Size: 41.2 KB (41162 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.5`

```console
$ docker pull kibana@sha256:5e64881ac2736d141b6bc2ce5c3aa1ca97ebba248a748a052411a6fff31a476d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.5` - linux; amd64

```console
$ docker pull kibana@sha256:447e011e1a27c2a0b2d36c5e07eaee65c4886343142a1cdec94f4f552f1781fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.0 MB (468020311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7f9836bb1bb21de97d2590fffa8bf5c95fd6030ee7e40288fc955038a9d3f0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:15:02 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 15 Jun 2026 23:15:02 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:23:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 15 Jun 2026 23:23:52 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:23:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 15 Jun 2026 23:23:53 GMT
RUN fc-cache -v # buildkit
# Mon, 15 Jun 2026 23:23:53 GMT
WORKDIR /usr/share/kibana
# Mon, 15 Jun 2026 23:23:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 15 Jun 2026 23:23:53 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:23:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:23:53 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 15 Jun 2026 23:23:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:23:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 15 Jun 2026 23:23:55 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 15 Jun 2026 23:23:55 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 15 Jun 2026 23:23:55 GMT
LABEL org.label-schema.build-date=2026-05-25T11:35:15.942Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T11:35:15.942Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Mon, 15 Jun 2026 23:23:55 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 15 Jun 2026 23:23:55 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:23:55 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 15 Jun 2026 23:23:55 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 15 Jun 2026 23:23:55 GMT
USER 1000
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3445ade83d2d9a959805ff76f06a7e09206f51d5a9cc63b66c31d81432389808`  
		Last Modified: Mon, 15 Jun 2026 23:24:56 GMT  
		Size: 19.3 MB (19331423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebf50602ef135166b240380f9b45c4c8ed4e4fc90ee0280397a114c4f42b854`  
		Last Modified: Mon, 15 Jun 2026 23:25:04 GMT  
		Size: 391.5 MB (391450280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d46e107440afcf1997c5c926841c0f9fd84ff72696c5047984e6d3ab161f4ca`  
		Last Modified: Mon, 15 Jun 2026 23:24:55 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f82d2956c912bddd4a4368689813f374d491b74b1cb76fcb3868e34e84290`  
		Last Modified: Mon, 15 Jun 2026 23:24:56 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50e8e4f120e97b431caf844674d28c5f0c726affd447f028c3538b1976daca6`  
		Last Modified: Mon, 15 Jun 2026 23:24:56 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52530c6999b35ddb884d3381ad7497e80948b8a47ca2970ee96eeb000e028fa4`  
		Last Modified: Mon, 15 Jun 2026 23:24:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6e5941ba5dbe4ea195a7c833f8dab5f69451dc98a4f3e279c9a9048a434f55`  
		Last Modified: Mon, 15 Jun 2026 23:24:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210367933a48e779a067629a66f23630787f70cf5a9a5824d95a9f3ea55e8091`  
		Last Modified: Mon, 15 Jun 2026 23:24:58 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd895138834a5548d1c8b4c533997cbbabe49e208a21021911a062363b8db87`  
		Last Modified: Mon, 15 Jun 2026 23:24:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00a2148e823ed908790b4863ae8c42b0f2b13be1b073fce801f1f3d40319b0f`  
		Last Modified: Mon, 15 Jun 2026 23:24:59 GMT  
		Size: 74.5 KB (74547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a62c736288236f11a7e372e9eba390f31084890ac9030a3780193057e4e4c4d`  
		Last Modified: Mon, 15 Jun 2026 23:24:59 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81de27e76ad0a15360e9afb54d4df0b0f0ca596f0fea7cd7cd6b061854b632af`  
		Last Modified: Mon, 15 Jun 2026 23:25:00 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.5` - unknown; unknown

```console
$ docker pull kibana@sha256:6e81c87d5a944aa4a1388b297cca327f7ce3bebf763bbf150208159382c5a9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e3193e485cb8e64fee940092d7212eac3a4d9d4da905b6138c9dceda2d8d82`

```dockerfile
```

-	Layers:
	-	`sha256:3ea680ee843e5da7972d04b8d5e8ed78d379476c6fb624748895ec641a0263a1`  
		Last Modified: Mon, 15 Jun 2026 23:24:55 GMT  
		Size: 5.9 MB (5886976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adde708ad5f7d6ebee6947cc5b9cdb6f93fd232f9fc64ffe399a07dd478b16ea`  
		Last Modified: Mon, 15 Jun 2026 23:24:55 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:504b46c06a3efcbcbb12236fcd597b15f56b37446136d4c7cd816ffff1fc752e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (478951780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42bf96b63c24dacc6021869090a9dd3668669ecdfcd5dc26dc5a9d8a5b1efdf`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:23 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 15 Jun 2026 23:14:23 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:21:23 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 15 Jun 2026 23:21:23 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:21:23 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 15 Jun 2026 23:21:24 GMT
RUN fc-cache -v # buildkit
# Mon, 15 Jun 2026 23:21:24 GMT
WORKDIR /usr/share/kibana
# Mon, 15 Jun 2026 23:21:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 15 Jun 2026 23:21:24 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:21:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:21:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 15 Jun 2026 23:21:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:21:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 15 Jun 2026 23:21:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 15 Jun 2026 23:21:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 15 Jun 2026 23:21:26 GMT
LABEL org.label-schema.build-date=2026-05-25T11:35:15.942Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T11:35:15.942Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Mon, 15 Jun 2026 23:21:26 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 15 Jun 2026 23:21:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:21:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 15 Jun 2026 23:21:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 15 Jun 2026 23:21:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cac6044fa98a6d73908e0d73210abf24c475da1c7ad0739835bd49d8cc79a7`  
		Last Modified: Mon, 15 Jun 2026 23:22:34 GMT  
		Size: 19.3 MB (19291910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f669a8424ffdfd4da48d9800c447a8987e0a448c4e63ad587b003ef60416c37`  
		Last Modified: Mon, 15 Jun 2026 23:22:41 GMT  
		Size: 404.2 MB (404229938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1680232962695c0d3e5195e8e72e1f8e57c5481ff16a350a8936a0966b56ab`  
		Last Modified: Mon, 15 Jun 2026 23:22:32 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6199782d8716d11435916ec47a97650b9934f74732307531686fa8e997f987`  
		Last Modified: Mon, 15 Jun 2026 23:22:34 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d267da64cb0bcae680a763fe8368da4264443b5cb9c9580fa846b3c26f9326b4`  
		Last Modified: Mon, 15 Jun 2026 23:22:33 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9959a7c6628dc2d2a4f4d5cfa3d986a12a03fcce197a789457f92816a6dbb370`  
		Last Modified: Mon, 15 Jun 2026 23:22:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3522124840017c3f753808eeda4a49e200975df9bee0909e5b314489d7df87`  
		Last Modified: Mon, 15 Jun 2026 23:22:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f461a02d216debe673ce1383d3d1c57ef1607eaaa31bd358a391728e442f6ce8`  
		Last Modified: Mon, 15 Jun 2026 23:22:35 GMT  
		Size: 4.9 KB (4920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00433333c1d443617cb922da7f42144ce7c86b2150ee21634a787ad2924f0027`  
		Last Modified: Mon, 15 Jun 2026 23:22:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46db66bcf619eba178dda0cb8aafb26078e5ff74b6f3451e98557a92c3c1b4b`  
		Last Modified: Mon, 15 Jun 2026 23:22:37 GMT  
		Size: 73.5 KB (73456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19fa0b57c0193842aa84ef58cfb366e2cd846cb5aa11ff9e1c1ecb6fc2a448a`  
		Last Modified: Mon, 15 Jun 2026 23:22:37 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fc509a8a7ececeaeefc9da1a31dc3e5a2c638a85018adddf3918ce6d09026d`  
		Last Modified: Mon, 15 Jun 2026 23:22:38 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.5` - unknown; unknown

```console
$ docker pull kibana@sha256:10d40a82193d4ca1df9d816f88151940af47fda1e9cf48fc6dd53ea1fa6cbc1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5929131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea5684d265ad0eeab45541f9fbf2598c5b45804024675266c7b5db5bd51d97d`

```dockerfile
```

-	Layers:
	-	`sha256:f472ba5ff6de5b9db9056891051d016f6146a15c695e54e676d142213cc13a64`  
		Last Modified: Mon, 15 Jun 2026 23:22:33 GMT  
		Size: 5.9 MB (5885648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5bd3d1785b38f2cda75d274e84cd471f70faab031b481165fd6243dda27eb74`  
		Last Modified: Mon, 15 Jun 2026 23:22:32 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.2`

```console
$ docker pull kibana@sha256:893fcc37b407aa251f5905a9a4fa9861b7a8bff93aae67ea1f9dc06d3828ed55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:771f5052d3bde861e8caac89cefba84daf13c85c1b2f51e690b3832537c65aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535319903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd101cc2118218bf165c6c1e0c21acdbed9bb734c65d9ec1d6828d00330142d7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:15:01 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 15 Jun 2026 23:15:01 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:24:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 15 Jun 2026 23:24:58 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:24:58 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 15 Jun 2026 23:24:58 GMT
RUN fc-cache -v # buildkit
# Mon, 15 Jun 2026 23:24:58 GMT
WORKDIR /usr/share/kibana
# Mon, 15 Jun 2026 23:24:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 15 Jun 2026 23:24:58 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:24:58 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:24:58 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 15 Jun 2026 23:24:58 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:24:59 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 15 Jun 2026 23:25:00 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 15 Jun 2026 23:25:00 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 15 Jun 2026 23:25:00 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Mon, 15 Jun 2026 23:25:00 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 15 Jun 2026 23:25:00 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:25:00 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 15 Jun 2026 23:25:00 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 15 Jun 2026 23:25:00 GMT
USER 1000
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03303764d74341920a112fddeea026c6ef64bad50ef12c3c15304cb88021a536`  
		Last Modified: Mon, 15 Jun 2026 23:26:09 GMT  
		Size: 19.3 MB (19331509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfd0280530affaf0deb41c25c13af8961c8e2188c0781f5e692e4b83dfa6c01`  
		Last Modified: Mon, 15 Jun 2026 23:26:18 GMT  
		Size: 458.7 MB (458749804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c63e392f0832fd14796caf17d551be0877366b0840c09854c1374117a20f2de`  
		Last Modified: Mon, 15 Jun 2026 23:26:08 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701b94b2d48e847103650cfee7f29223a094bb4ce19a2f2e496446aee7becc2e`  
		Last Modified: Mon, 15 Jun 2026 23:26:09 GMT  
		Size: 16.5 MB (16460478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f172491775199df24d30914f6f72799e04a93a37118931940cbae121921a3e`  
		Last Modified: Mon, 15 Jun 2026 23:26:09 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f544a03a086d3b381ab4c7a8cce004f7d34cdac17986ab0520044f7ee90ade`  
		Last Modified: Mon, 15 Jun 2026 23:26:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1544fda3e9263ed6571c43da5abe19d97c5211e9b9c72d8cf23f6f55b8017447`  
		Last Modified: Mon, 15 Jun 2026 23:26:11 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645715d8e46bd2790e9b8268a553d0b3082090bd1cc34d81d7cf0d07d0290fb3`  
		Last Modified: Mon, 15 Jun 2026 23:26:11 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87ee43004a8cc06f4fa9c331806b16a501fdf6e1dadf3e5230c933288a0f44a`  
		Last Modified: Mon, 15 Jun 2026 23:26:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91907d2d03dc1db5f5661ca6a0e654af3799954773eac5dd7337d6ba99f3b38`  
		Last Modified: Mon, 15 Jun 2026 23:26:12 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a363ef5065021bb4942ccf28fca9ada4697b24cebc18873f90fc7c8ac8b88e`  
		Last Modified: Mon, 15 Jun 2026 23:26:13 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8913281e1a4b3eaab94f914375f3e06f78e6377194bd9c933de4b971e19315`  
		Last Modified: Mon, 15 Jun 2026 23:26:13 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:f2489eccb3a0790243dd6786be74cc93eb65e832b34575b6b84a11431eaf304b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab4ee928c667fd166b70c2bcd8ff6d5655a21abbdf0f2ee81e28bf0be033e89`

```dockerfile
```

-	Layers:
	-	`sha256:8f317e9f1ce6f07a6971e1f8038ff8f9fec6664c8786310dc0ff0b6029589816`  
		Last Modified: Mon, 15 Jun 2026 23:26:09 GMT  
		Size: 6.0 MB (6021103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc95c9949253d9b5b2ee58fb3a01393ae044b7eb9f38b9d3005fb8bc2c875e0`  
		Last Modified: Mon, 15 Jun 2026 23:26:08 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:bc629ee5d170e58e6bf7b4a179c15b9c792d72f0afd63f6ff71070fb9398d3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546337834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25b31f2175a0907f25cdef83a31aa18e908d0475424dd8a23ad8e8194f69cf0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:14:26 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 15 Jun 2026 23:14:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:22:21 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 15 Jun 2026 23:22:22 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 15 Jun 2026 23:22:22 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 15 Jun 2026 23:22:22 GMT
RUN fc-cache -v # buildkit
# Mon, 15 Jun 2026 23:22:22 GMT
WORKDIR /usr/share/kibana
# Mon, 15 Jun 2026 23:22:22 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 15 Jun 2026 23:22:22 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 15 Jun 2026 23:22:22 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:22:22 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 15 Jun 2026 23:22:22 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 15 Jun 2026 23:22:23 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 15 Jun 2026 23:22:24 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 15 Jun 2026 23:22:24 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 15 Jun 2026 23:22:24 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Mon, 15 Jun 2026 23:22:24 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 15 Jun 2026 23:22:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 15 Jun 2026 23:22:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 15 Jun 2026 23:22:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 15 Jun 2026 23:22:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606003fbd75bf88c936fcd7823d9d99a98c00705e6cd820ffac46421c808b888`  
		Last Modified: Mon, 15 Jun 2026 23:23:47 GMT  
		Size: 19.3 MB (19291848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a903cc3c08c56dfcdc5c4e2e7506f7cfc1b943957e462958b932e52cfe73c`  
		Last Modified: Mon, 15 Jun 2026 23:23:56 GMT  
		Size: 471.6 MB (471616066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1e52b2c77841909cffda5488e00346649be7408e001da188b9162335f68875`  
		Last Modified: Mon, 15 Jun 2026 23:23:45 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666764dc3402d093773909d3afe7b953b10548b027b26929d3cde115829390f5`  
		Last Modified: Mon, 15 Jun 2026 23:23:47 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a826325258575503b9421c2cb5cabe28e86e48e90a7c0bb6f51ad24b44c8fc2`  
		Last Modified: Mon, 15 Jun 2026 23:23:47 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8827e1738978bd5bdc15b41c72ea0ba3919aba8be134eea9b44c9edee33b86de`  
		Last Modified: Mon, 15 Jun 2026 23:23:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5727f60b70a4663b656491e35f3ab2421eea05fa1df437684a58b79ac62f2a9d`  
		Last Modified: Mon, 15 Jun 2026 23:23:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3ed9c571580a9b9d214ee3cc336da225655bd2e7213a545fae1751dadc5cb`  
		Last Modified: Mon, 15 Jun 2026 23:23:48 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fa1eb10e73a49dc43091bc6dc4b7cca13805d5d1b305ff0c19cb949b1c36d6`  
		Last Modified: Mon, 15 Jun 2026 23:23:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fbf39569ef53ff2a745d5fe5943c9a08c01f0062a3f16730a291a7621b91ed`  
		Last Modified: Mon, 15 Jun 2026 23:23:49 GMT  
		Size: 73.5 KB (73455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a12da2aaba365cf618c98757e8ffb130e77648d4e0c5faf702162dd6a30a3ad`  
		Last Modified: Mon, 15 Jun 2026 23:23:50 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ecd73ecf8c7543b4c5fe549065e2d8b401dff5cac24422c79cecc47c1a28bd`  
		Last Modified: Mon, 15 Jun 2026 23:23:51 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:9e2a2c93560a170b9a3ac27321984d4bab178627556d3cd872f9204b0109c8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6063258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a696df3d54a86b9246abafe6f26b6aa5c7ce88a0c92a0d7b8d0cb7182e09cb55`

```dockerfile
```

-	Layers:
	-	`sha256:dd3367012e82a9b0463b2e4ebbc0bb31e0a9f6b70e38f77410e9be4ee76efc3b`  
		Last Modified: Mon, 15 Jun 2026 23:23:46 GMT  
		Size: 6.0 MB (6019775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a6acadb5ccc720ee4b0aab6afdc04486d4caa2bbc4b57e7fee15c9120b2350b`  
		Last Modified: Mon, 15 Jun 2026 23:23:45 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
