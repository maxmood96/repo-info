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
$ docker pull kibana@sha256:1bafa44796d1f81a2cd2e241a3bc8cdc600b25bd11cb1769588c06a0de7050bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.5` - linux; amd64

```console
$ docker pull kibana@sha256:9ebe2fe5427feefb283ba05b535863a5c57250c8ffcc3714266c95b5f4f1450e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.1 MB (468050742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e3d7063ed273b19d66eaaab54917d047d02d2b1fb8cce0f6e9c7134e000302`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Thu, 28 May 2026 21:35:15 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 May 2026 21:35:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 28 May 2026 21:43:55 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 May 2026 21:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:43:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 May 2026 21:43:56 GMT
RUN fc-cache -v # buildkit
# Thu, 28 May 2026 21:43:56 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2026 21:43:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 May 2026 21:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:43:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:43:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 May 2026 21:43:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:43:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 May 2026 21:43:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 May 2026 21:43:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 May 2026 21:43:58 GMT
LABEL org.label-schema.build-date=2026-05-25T11:35:15.942Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T11:35:15.942Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Thu, 28 May 2026 21:43:58 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 28 May 2026 21:43:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:43:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 May 2026 21:43:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 May 2026 21:43:58 GMT
USER 1000
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e808313f0a9000e128993cda3a75b07394a879ecf482845e057183d8d23fab3`  
		Last Modified: Thu, 28 May 2026 21:44:55 GMT  
		Size: 19.3 MB (19332187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa5c2d24f4e7c0f10b7cc7b8fdcc6c0f94f059d408ffa686c5983b34e242044`  
		Last Modified: Thu, 28 May 2026 21:45:05 GMT  
		Size: 391.5 MB (391451435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a17d0aadc535e78ae87e486f9832ef392e57c84c18b5dad0227a2ab0e2371`  
		Last Modified: Thu, 28 May 2026 21:44:54 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34e34e7df1004481a2d339a8ea84ee96919ad3c5b9d4423003bd6f3b54f733b`  
		Last Modified: Thu, 28 May 2026 21:44:55 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4aaf7fc7c309b02c3f23efdfe0f6cecf7a98f74efff7f24851a62fbbbefc9c`  
		Last Modified: Thu, 28 May 2026 21:44:55 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521e915f8581370012a8ab50ecc971473c0348126531cbdb9b4cad90e92a2178`  
		Last Modified: Thu, 28 May 2026 21:44:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac4deef9ea9a1289b039ce93d2fb2284f14ddfa35fa9f865a3e42d0aff0801`  
		Last Modified: Thu, 28 May 2026 21:44:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d969982d38358e4a25e57ad3e69c68a3129e67541fe08bbe91ffc711d8b5dc`  
		Last Modified: Thu, 28 May 2026 21:44:57 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e334b5ab224a12ae5029e278b215cd008b40268353aad1d98c3db59922cb7c35`  
		Last Modified: Thu, 28 May 2026 21:44:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf3fc844d0098e10f41076aef23b52b5bd9b8320deb91c3d044802d5ae03ee1`  
		Last Modified: Thu, 28 May 2026 21:44:58 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c5d145ce52ed2af225ac5c243410d52d177bb250eabd9097d3f36a0619fde`  
		Last Modified: Thu, 28 May 2026 21:44:58 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe8283d488ab0ef304231d2bacc6146ab6ecfe8035d125854fd06bbec09d06e`  
		Last Modified: Thu, 28 May 2026 21:45:00 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.5` - unknown; unknown

```console
$ docker pull kibana@sha256:e7697e37df025c828736bacd3ab15c4726c11e79168281638fa3054e338300c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693f9501cd9235c46254feb00a62f0de9e370b35cdeb58ecdfbce2b0c24b2a83`

```dockerfile
```

-	Layers:
	-	`sha256:2292b2644b2cea1fb4c0f12f31cc92b23a6dbfb83b1efc0fa984d46e9416e510`  
		Last Modified: Thu, 28 May 2026 21:44:55 GMT  
		Size: 5.9 MB (5886964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:261c8e2043d49054447a3e1e6bbe6587d4683c2bc0329e5d5934122aa29ad706`  
		Last Modified: Thu, 28 May 2026 21:44:54 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a260b8d92f300638adabefc72f452824f5d6de01a139ce5e515a7a58e75bd95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.9 MB (478911253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129af864bb7594daa890a4659d8cddc1d98871675c16cd24d1b534d167de95ef`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Thu, 28 May 2026 21:34:10 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 May 2026 21:34:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 28 May 2026 21:41:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 May 2026 21:41:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:41:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 May 2026 21:41:09 GMT
RUN fc-cache -v # buildkit
# Thu, 28 May 2026 21:41:09 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2026 21:41:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 May 2026 21:41:10 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:41:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:41:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 May 2026 21:41:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:41:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 May 2026 21:41:11 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 May 2026 21:41:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 May 2026 21:41:12 GMT
LABEL org.label-schema.build-date=2026-05-25T11:35:15.942Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T11:35:15.942Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Thu, 28 May 2026 21:41:12 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 28 May 2026 21:41:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:41:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 May 2026 21:41:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 May 2026 21:41:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fb8c28a7b9236f44aafe18e985cd2f3e645e2e8028693efa3c3b24f3d6ebc7`  
		Last Modified: Thu, 28 May 2026 21:42:20 GMT  
		Size: 19.3 MB (19293891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93070387a62a4333941b6c0af536893fc73d4d5bfa4936425b038a305a94dda1`  
		Last Modified: Thu, 28 May 2026 21:42:29 GMT  
		Size: 404.2 MB (404220310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e368fba5a3fd12d73b9c865759c7f0d1aaff07a386451bad543eb0d61b39567b`  
		Last Modified: Thu, 28 May 2026 21:42:19 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9592b8f1b5e027e6fb4279049a7d5ce972565c4479ad3c5060d5071447e56de4`  
		Last Modified: Thu, 28 May 2026 21:42:20 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4eb3bbcdb007e98d8bf73b8b833531a9765d4189ce6be91f253d6f20ec1480`  
		Last Modified: Thu, 28 May 2026 21:42:20 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a288280b48391ef116a658b44684b3faadfc397ab7205fed9860e20c52c8a02b`  
		Last Modified: Thu, 28 May 2026 21:42:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae8e86fd8c95c57de0fdb50799906017907c12ec332ac8351f659e681400baf`  
		Last Modified: Thu, 28 May 2026 21:42:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5201497bf165c62cc1aeb2af466d5429e603781d11ed408c284d123bdd289c36`  
		Last Modified: Thu, 28 May 2026 21:42:22 GMT  
		Size: 4.9 KB (4920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a362aee8147e5ad76b49b9a16ef3cb00ecef62e1959accafea8ddef973d081`  
		Last Modified: Thu, 28 May 2026 21:42:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c486d1a1c57b804e3ae4a3d0f832bc0e3e07bc5b2742aa5a5297d8e4977558`  
		Last Modified: Thu, 28 May 2026 21:42:23 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134eb38d231999b115d1d910598fd9320ec9d851880b660c02096f5385aad60`  
		Last Modified: Thu, 28 May 2026 21:42:23 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd73180f9b0ac40d2a9b2962f59f605b53996105281b100c25d2ee23891f3df5`  
		Last Modified: Thu, 28 May 2026 21:42:24 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.5` - unknown; unknown

```console
$ docker pull kibana@sha256:97d5f69e6baf1a98fb6fcabd6878bec6d45f2f0c37707c133cc3620219f18208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5929119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3348cab5873c951219927d30acb61890587ebe5d9aec1ca0fdf5e8c7c987b34`

```dockerfile
```

-	Layers:
	-	`sha256:f7854d88b66d3d7bf149d74e6beefea49d58458d1f9ba58092ee918cb4dbfa8b`  
		Last Modified: Thu, 28 May 2026 21:42:19 GMT  
		Size: 5.9 MB (5885636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574b17e885b195bafa078b9a0264ffe76d43d509985a13bb0f5b3cd9e4089d59`  
		Last Modified: Thu, 28 May 2026 21:42:18 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.2`

```console
$ docker pull kibana@sha256:8fcd9f6e0f6c7ef7a9642ea6aa547d6331901dec716a15cc08e6e4f2ae85f143
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:c0baa6b792be51a78d827e76e63183b25f735f44998204c951a23cfbbd96631c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.4 MB (535351839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6615ee1afba93d23bb10b61db0757d12877117b7056087e8882c7cdea3e7530e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Thu, 28 May 2026 21:34:59 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 May 2026 21:34:59 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 28 May 2026 21:44:29 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 May 2026 21:44:30 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:44:30 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 May 2026 21:44:30 GMT
RUN fc-cache -v # buildkit
# Thu, 28 May 2026 21:44:30 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2026 21:44:30 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 May 2026 21:44:30 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:44:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:44:30 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 May 2026 21:44:30 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:44:31 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 May 2026 21:44:32 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 May 2026 21:44:32 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 May 2026 21:44:32 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 28 May 2026 21:44:32 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 28 May 2026 21:44:32 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:44:32 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 May 2026 21:44:32 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 May 2026 21:44:32 GMT
USER 1000
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d730f7ca7802d5452896ccbcd343b4bb5e93baa944dde11be4d55daee07eb4e`  
		Last Modified: Thu, 28 May 2026 21:45:49 GMT  
		Size: 19.3 MB (19332176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e48fc409452cda048e49919f2559684ae3e04b60be55e19da12acc68ea030c`  
		Last Modified: Thu, 28 May 2026 21:45:58 GMT  
		Size: 458.8 MB (458752546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35c31c78125499b0934ccd952f84ff6fcfc5f4816b327fea556ef0c4732f4f`  
		Last Modified: Thu, 28 May 2026 21:45:48 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b502b665bd2dae2dc9f421dd8867c9f8e7fdf71fd3a3c7369d34a7d57b09bf`  
		Last Modified: Thu, 28 May 2026 21:45:49 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b80299c62a46f0cac541644d361c773ac68f776317c485c1d59f88b3aab0f4c`  
		Last Modified: Thu, 28 May 2026 21:45:49 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4a4d1f7ce07dd240944a28a39e5de834979ad7a880b2c5b11fcedaa584b541`  
		Last Modified: Thu, 28 May 2026 21:45:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d66fcd4b7f6a4196c90342e8d4705f514ffcfc99a74de19b475dfe07adcca`  
		Last Modified: Thu, 28 May 2026 21:45:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d648a61681b8fe5899f55ee7ea847079d1aca8aeb305780b2a7e9cee9f7e6838`  
		Last Modified: Thu, 28 May 2026 21:45:51 GMT  
		Size: 4.9 KB (4920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c87533f2c231bb0c0d7c4ebf57e862c8c3ee2cc0311ad76100b873e151bd25`  
		Last Modified: Thu, 28 May 2026 21:45:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177df8dece213a87a495969efda338267060c10403cbe090f69219825ebf44cb`  
		Last Modified: Thu, 28 May 2026 21:45:52 GMT  
		Size: 74.5 KB (74545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49eab644df329114a99a77e9e92d324b209b062a84683921a00e60d851fa49`  
		Last Modified: Thu, 28 May 2026 21:45:52 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc4cd3318f36f4f3b5eaaa8242c8a83082f1b4af8ce394d3474c917a077468b`  
		Last Modified: Thu, 28 May 2026 21:45:53 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:af123fddb0dc261a214c15431361ede44da32882f87329ade1c819d68cee9a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbf79757e01455bdf751207dc626bb48110c2fd05cf72363e01c53dc0b9e086`

```dockerfile
```

-	Layers:
	-	`sha256:2d519a9b0d9875d0ab5549de68f6499f659c80d229ba8c8cc2b79163a9393a32`  
		Last Modified: Thu, 28 May 2026 21:45:48 GMT  
		Size: 6.0 MB (6021091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abe211d8c827d99df7c5805b0ff751432738906796a6094067bf220030e4aee`  
		Last Modified: Thu, 28 May 2026 21:45:48 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1e27e1323351ad3d966653fbc970c5b02e3580a39bb50f4849b4672b8cbb0edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546306233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2e814d344c25f77163db0c1988ff2c5e5624d23697244607351943ec66702`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Thu, 28 May 2026 21:35:03 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 May 2026 21:35:03 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 28 May 2026 21:42:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 May 2026 21:42:49 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:42:49 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 May 2026 21:42:49 GMT
RUN fc-cache -v # buildkit
# Thu, 28 May 2026 21:42:49 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2026 21:42:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 May 2026 21:42:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:42:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:42:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 May 2026 21:42:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:42:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 May 2026 21:42:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 May 2026 21:42:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 May 2026 21:42:52 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 28 May 2026 21:42:52 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 28 May 2026 21:42:52 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 28 May 2026 21:42:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 May 2026 21:42:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 May 2026 21:42:52 GMT
USER 1000
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e11ea7cc2002a7283e50ada3baaeb4c3fed975667f9d61ba023fab58abe57c`  
		Last Modified: Thu, 28 May 2026 21:44:14 GMT  
		Size: 19.3 MB (19293842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cf9213947174fce8dcc56494dd631bc18798519be404fe3d4b38459eacafbe`  
		Last Modified: Thu, 28 May 2026 21:44:22 GMT  
		Size: 471.6 MB (471615359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5d18eedd4890a1e9f0f9bc9c881c63ad3e5fa14452af48405f90bab1122243`  
		Last Modified: Thu, 28 May 2026 21:44:12 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5ed01c6eb1c148336b2af6bf82badf200524b19b0a82295b0548dd5787d93f`  
		Last Modified: Thu, 28 May 2026 21:44:15 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dfb1625c803c4ff8f55b163d0f5153b876235831cb379e11268d9679644bc0`  
		Last Modified: Thu, 28 May 2026 21:44:14 GMT  
		Size: 5.2 KB (5220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc8da79dfb651341152f320fba546a3e9b78d1f26b917d117473ab6271b5fff`  
		Last Modified: Thu, 28 May 2026 21:44:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0c6b53ef3dc2e9300e00e3374f383f3986a0684c049bd4c61c3e609716f784`  
		Last Modified: Thu, 28 May 2026 21:44:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a96b65c11431afcee173972b049cf1cfe4f002f220c2486b9ce3a175070de9e`  
		Last Modified: Thu, 28 May 2026 21:44:16 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b51f3dcd281e96d5cbbcb6e71371aaeace289d33c182224589e17a391493d12`  
		Last Modified: Thu, 28 May 2026 21:44:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ea1f36ae853bcb2137a044ea46b670d2ca394b1960fed201cddadc54e8f901`  
		Last Modified: Thu, 28 May 2026 21:44:16 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e0183ee8e968bac050c82edddb111a581c9e86b56808048db19a940ff6e79e`  
		Last Modified: Thu, 28 May 2026 21:44:17 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ebb86e3c914edfb7dfac66b87120fa3dfa6e2237a7e147a5a56eb25cb70fe7`  
		Last Modified: Thu, 28 May 2026 21:44:18 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:d4f89f298bf91f5e938498ce78a6efb72ec9ad0dde7d45f1b39a98eb4e8bb5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6063246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2891b2c9c66aeb735132cba3f27c804d51e1ffe411bdf676e03d57b0ca14676d`

```dockerfile
```

-	Layers:
	-	`sha256:ed4832ab56fd5b4268a602b64e469fbc23285cfccec0f6a23a41df8d62d710b3`  
		Last Modified: Thu, 28 May 2026 21:44:13 GMT  
		Size: 6.0 MB (6019763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b163a4044314cfbefeaac83f7df3ab365c67b44d8eea6f94f1c71144d1b0ca20`  
		Last Modified: Thu, 28 May 2026 21:44:12 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
