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
$ docker pull kibana@sha256:a1026503e5facaca2cb90e56ce0b1fe430d2399022226168170890c8d1c311a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.5` - linux; amd64

```console
$ docker pull kibana@sha256:34a06f19c9176e1701e28b20c02326ea6b9135ec4673b8b2b893573d2b655c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.0 MB (468026834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b36862556cf50f5057d1b9884a2507a624fad5d8286cf9aaa2ea78008b8f25e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:46:07 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Jun 2026 22:46:07 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:55:03 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Jun 2026 22:55:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:55:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Jun 2026 22:55:04 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Jun 2026 22:55:04 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Jun 2026 22:55:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Jun 2026 22:55:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:55:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:55:05 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Jun 2026 22:55:05 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:55:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Jun 2026 22:55:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Jun 2026 22:55:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Jun 2026 22:55:06 GMT
LABEL org.label-schema.build-date=2026-05-25T11:35:15.942Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T11:35:15.942Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Tue, 02 Jun 2026 22:55:06 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Jun 2026 22:55:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:55:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Jun 2026 22:55:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Jun 2026 22:55:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3c38ed11716605bb2ef20cbe3fb3305dcf6cc17d0f900a3c65ff5057c7522f`  
		Last Modified: Tue, 02 Jun 2026 22:56:09 GMT  
		Size: 19.3 MB (19332300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e2205c4cab44425abb6a5926e6206ae2ba27eb5d6beffd51760efabe664b8`  
		Last Modified: Tue, 02 Jun 2026 22:56:17 GMT  
		Size: 391.4 MB (391449069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01188b78c5b0d73c58c82f1758af33155cda9cb048b98ea61e315c70ae3e21f`  
		Last Modified: Tue, 02 Jun 2026 22:56:08 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95e8d15fba33d0514b51842654bcfb665f167034bc2b1918d1ccacbea8c568`  
		Last Modified: Tue, 02 Jun 2026 22:56:10 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61bda820a40a9af4d6b8bacee1a820e07148d328a606f50252c899357a90fa5`  
		Last Modified: Tue, 02 Jun 2026 22:56:09 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af38529f6153c2406346916f53faa12e6496c7452748c22fd871b3d5a1b3cac`  
		Last Modified: Tue, 02 Jun 2026 22:56:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085e1b995fc38e6743526b2ce5419ee4a8b08b71641a177e475099381a2ff9ad`  
		Last Modified: Tue, 02 Jun 2026 22:56:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfea7e63ef5e6dc6e921f12a349a36348625bce76b1dad957e676d748f50709`  
		Last Modified: Tue, 02 Jun 2026 22:56:11 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce05440c608b947b32abb1161ae30f59bab22fb011616f5ed907b30828a1b96`  
		Last Modified: Tue, 02 Jun 2026 22:56:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faef8e20c9462a2d4b3240e9871a739adb50b1705452a8a32241d6469571b60e`  
		Last Modified: Tue, 02 Jun 2026 22:56:13 GMT  
		Size: 74.5 KB (74545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606a1324fb66e373015a3491e0eae339d9f34b3970948b58f3528ac1b3398901`  
		Last Modified: Tue, 02 Jun 2026 22:56:13 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5718e1450a77f41108eba81d4bb99ba747f7c3c805a0f1f9287abd07d96bfe0`  
		Last Modified: Tue, 02 Jun 2026 22:56:14 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.5` - unknown; unknown

```console
$ docker pull kibana@sha256:5842c6e1c7f89d54719053cd2e4db79f0e7ae2e911bb34fffb4163ec1292b944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5930190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320abdcb7e89bbc6ae157cadb117b0d38141fa7da3837e4f75dc6903c93829f3`

```dockerfile
```

-	Layers:
	-	`sha256:2f50fc8369a1053d6fbcf28903afeaf89b9e8aca4e47cc52f43d26ef670a727f`  
		Last Modified: Tue, 02 Jun 2026 22:56:09 GMT  
		Size: 5.9 MB (5886964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818404fe2377ba6629bff884a4682d49b2ec0d298c6815ef85a83bda913709c8`  
		Last Modified: Tue, 02 Jun 2026 22:56:08 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:dfdc587d88611a7cece0167d22db854d900f7eb5fb7baad28ec9f0288efbc46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.9 MB (478935082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d422a09993499e416672d5ee02c8ca397cbfadae3302015a7d38ac49fb5640`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:39 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Jun 2026 22:45:39 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:52:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Jun 2026 22:52:58 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:52:58 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Jun 2026 22:52:58 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Jun 2026 22:52:58 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Jun 2026 22:52:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Jun 2026 22:52:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:52:58 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:52:58 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Jun 2026 22:52:58 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:52:59 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Jun 2026 22:53:00 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Jun 2026 22:53:00 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Jun 2026 22:53:00 GMT
LABEL org.label-schema.build-date=2026-05-25T11:35:15.942Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-25T11:35:15.942Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db396449a69d0613b0b4dc8b8e9789aa35504e0f org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5
# Tue, 02 Jun 2026 22:53:00 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Jun 2026 22:53:00 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:53:00 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Jun 2026 22:53:00 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Jun 2026 22:53:00 GMT
USER 1000
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb55ca067bb77b05cd0ff47599419eb95f03c8e54c8ebc014afb365e9854ef`  
		Last Modified: Tue, 02 Jun 2026 22:54:08 GMT  
		Size: 19.3 MB (19291906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c217eee4cf8d51bd1ee3e30cbe803325d92904e3769d2802d1a9465017c4be1d`  
		Last Modified: Tue, 02 Jun 2026 22:54:16 GMT  
		Size: 404.2 MB (404223119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fef4f39572cf6998ea6828292e63a7cc23a95519e666481aba7874fb3759011`  
		Last Modified: Tue, 02 Jun 2026 22:54:08 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68c9b55e7eab6f3fbd6eb47eff959149de26ccef2e6d32484315c01569a03c`  
		Last Modified: Tue, 02 Jun 2026 22:54:08 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b884c0f993240ae6a07604e434dd178a17ad657f1dc1c743873f6456d7588`  
		Last Modified: Tue, 02 Jun 2026 22:54:09 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461af0375d5a626b2decf4b346d2b9a56256d1c343e09d31ce220eb7929ab611`  
		Last Modified: Tue, 02 Jun 2026 22:54:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2ca9634f41c66743afec07847d4e81a41ff58c758d3853ce4ca8a54aa6c5ec`  
		Last Modified: Tue, 02 Jun 2026 22:54:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787a90da1cdd4644c55432341a95a8f82a4026663154577ff9d99c42d729e3a8`  
		Last Modified: Tue, 02 Jun 2026 22:54:10 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85b0408ea76512e2920aca5e32e3663beaf8a9c1a27e1f98a72ed773feff1f`  
		Last Modified: Tue, 02 Jun 2026 22:54:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead1051b8b764c01e6f3e78868f0df5b9ad73208d55cadc36f1b962cbde68747`  
		Last Modified: Tue, 02 Jun 2026 22:54:11 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caa5f55833ddb377e7f688a57480616e9c5f4e6395264dc83d651055260514a`  
		Last Modified: Tue, 02 Jun 2026 22:54:12 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5cb24e9296e7882e595478563eae89c5ff49f126a26e3a375ab3ed35d91bb6`  
		Last Modified: Tue, 02 Jun 2026 22:54:13 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.5` - unknown; unknown

```console
$ docker pull kibana@sha256:0eb73fbe80bb17d60fc4b31f9b213e2992af6404a504f6e209b2f5fc857f7a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5929119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3804c89921d1749b44ec474f85bb94b14e61a4e3b90e945fb0cb34e236ca359`

```dockerfile
```

-	Layers:
	-	`sha256:20d292d3eb6755798187afdf7c18f1e8a2c11c60df0dd54ecf567511ec3ff7c7`  
		Last Modified: Tue, 02 Jun 2026 22:54:08 GMT  
		Size: 5.9 MB (5885636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0ab08263e8a7cdffa036697b337003cff45066b49712d567470a639e7fc77ce`  
		Last Modified: Tue, 02 Jun 2026 22:54:08 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.2`

```console
$ docker pull kibana@sha256:d26cd90c39633a360778298e2527bfad06a9a8341642fdf36919b915e9c5ab6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:3a4cbaa111498c6de3b241c8f25296d1e7d46055e04edd4662ca6157e39da82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535334056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d73fa32493bfbf9f8c704f38921759d0b9d7a8fbfd4a2114323eed8081187f3`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:46:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Jun 2026 22:46:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:54:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Jun 2026 22:54:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:54:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Jun 2026 22:54:13 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Jun 2026 22:54:13 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Jun 2026 22:54:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Jun 2026 22:54:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:54:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:54:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Jun 2026 22:54:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:54:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Jun 2026 22:54:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Jun 2026 22:54:15 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Jun 2026 22:54:15 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 02 Jun 2026 22:54:15 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Jun 2026 22:54:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:54:15 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Jun 2026 22:54:15 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Jun 2026 22:54:15 GMT
USER 1000
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d00ba161190b4345cc8ed79bdb2c755b6250b0238fab7b9321e80938deddd59`  
		Last Modified: Tue, 02 Jun 2026 22:55:30 GMT  
		Size: 19.3 MB (19332520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f979bfe98317f5e15af7864c9cc47c4de54790ca32a5b98f732c0af3473f96f`  
		Last Modified: Tue, 02 Jun 2026 22:55:38 GMT  
		Size: 458.8 MB (458756074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f954a6ef0b062fb9be2d0232312cc1a8622126fd24859d2300f6787a5c7a11c`  
		Last Modified: Tue, 02 Jun 2026 22:55:29 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa61e54434912308c573be296edd665fc2e501b00c993761d04c26b31bb37d`  
		Last Modified: Tue, 02 Jun 2026 22:55:30 GMT  
		Size: 16.5 MB (16460480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23562b868e05df3c801699f1b72f96014d7d534173bc8cf6fee55c2697ee936`  
		Last Modified: Tue, 02 Jun 2026 22:55:30 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8d80a1394000d4a8e74e3b3b71195bee1884214b05448e586154d0e2b45c37`  
		Last Modified: Tue, 02 Jun 2026 22:55:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1b6cb452a1659e5056b98464c87f42c8f562979b4a42f609255b9cda9895b4`  
		Last Modified: Tue, 02 Jun 2026 22:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb91de1929e22621897ab7e9c538de9b2d44a22f0ef64b3e3bfda7a5cdc97869`  
		Last Modified: Tue, 02 Jun 2026 22:55:31 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9558845865353879bf94369508023ab8d57bbcf737ba026b691c7bf3a8201a`  
		Last Modified: Tue, 02 Jun 2026 22:55:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b415e94a2491375302a2a31c2bdc41774c106ed25a0558c7f6f9338de910fa61`  
		Last Modified: Tue, 02 Jun 2026 22:55:33 GMT  
		Size: 74.5 KB (74547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c5ec4158126bae249bc6c11d1817860cbedc8cd58706236981b2a0abedb90b`  
		Last Modified: Tue, 02 Jun 2026 22:55:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd4379a7b24c31714cae66c4b18735115c793a5368c79b5bb9ea2009e74281a`  
		Last Modified: Tue, 02 Jun 2026 22:55:34 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:51593b36de30ea6f167ba694dd438595a7357f03d88b94e9aa50b8014df79b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a167a69a4f405a00b5ad1285053de576b84e7676a3782ac5a059a5b20890717`

```dockerfile
```

-	Layers:
	-	`sha256:433914187a04cd852ce230d00ef88cf3070537f50509955fef2263d17b8e9b57`  
		Last Modified: Tue, 02 Jun 2026 22:55:29 GMT  
		Size: 6.0 MB (6021091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb647161c4d60a2a19af05652486afbfcf26ea6749cfc8d49708b709e0094c3`  
		Last Modified: Tue, 02 Jun 2026 22:55:29 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:05e1cb8fde132668c1aad30fe0a0e0c834711810ad9494f818ce563386dcf442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546329762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d87e8f04503419314eaf57fe764129e707861fc6363d1e19134e4169983d44`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:39 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Jun 2026 22:45:39 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:53:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Jun 2026 22:53:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Jun 2026 22:53:48 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Jun 2026 22:53:48 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Jun 2026 22:53:48 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Jun 2026 22:53:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Jun 2026 22:53:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Jun 2026 22:53:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:53:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Jun 2026 22:53:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 22:53:49 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Jun 2026 22:53:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Jun 2026 22:53:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Jun 2026 22:53:51 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 02 Jun 2026 22:53:51 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Jun 2026 22:53:51 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Jun 2026 22:53:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Jun 2026 22:53:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Jun 2026 22:53:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441581a76f83d3aca1b7ab5a5c35358a8c48a9cd50358ccff1b4e46f292214fb`  
		Last Modified: Tue, 02 Jun 2026 22:55:12 GMT  
		Size: 19.3 MB (19291901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1322b2e62d52d836ef968d9d0ecfbe8ccc4699910f551fda5e44f9bef8075dd`  
		Last Modified: Tue, 02 Jun 2026 22:55:21 GMT  
		Size: 471.6 MB (471617815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378e704a0c252038a2972162f0894fc79d70771679c0b3ad2f68b2dc373d5cb`  
		Last Modified: Tue, 02 Jun 2026 22:55:10 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe810006da85016d1813a5baaec5af2175d1c7bc3e43a3cc1b50be6e2e50d61`  
		Last Modified: Tue, 02 Jun 2026 22:55:11 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a4da34ad9e95e9bd478568e14517447381912c3cbef56eb4ab34377a9341eb`  
		Last Modified: Tue, 02 Jun 2026 22:55:11 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caffdf05b0498244212cd2ce3802cd78c29f79f76bb3ac24f0c2a6057a109fe9`  
		Last Modified: Tue, 02 Jun 2026 22:55:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030df980a920ca017b7d793538995fee019bdfef8c7908c5e50725fff23c372d`  
		Last Modified: Tue, 02 Jun 2026 22:55:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6b6d5d14658f11da32fcc56483102e21d29590f7d9213f5e3ec6cc79eb0f51`  
		Last Modified: Tue, 02 Jun 2026 22:55:13 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeb1c0d7c4a40d17d8af78eba0b408ced1b98c84614005da01a25c989ff64c3`  
		Last Modified: Tue, 02 Jun 2026 22:55:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18e41aedb783333ceed0a2d0658c5a0263f5ae20508da22f01d0887017820d1`  
		Last Modified: Tue, 02 Jun 2026 22:55:14 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32595362ce5015c60fae3d512e4cd2cebc13ff84966e2e32774e61fd5b821671`  
		Last Modified: Tue, 02 Jun 2026 22:55:14 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6004d2026e7102405d982956c87185d1aeafd6ee506a9f6791169207c54c937`  
		Last Modified: Tue, 02 Jun 2026 22:55:15 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:9bce7692bdb72a3fae9a2558302d3bdb8a323d86ff8543af77b8266f2b4ee4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6063245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20305509efd64e28e27a8c703f919229852d711f47af78df2d0192983d992be5`

```dockerfile
```

-	Layers:
	-	`sha256:7bf6c04440e313c63f0f13c32bd326cf1c8ea9010d40558ee6a9e38726e27131`  
		Last Modified: Tue, 02 Jun 2026 22:55:11 GMT  
		Size: 6.0 MB (6019763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d406a74eaae65a5fec1e871b3b26e6815152cc0d191b5d02fea513d5f69c7eb`  
		Last Modified: Tue, 02 Jun 2026 22:55:10 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json
