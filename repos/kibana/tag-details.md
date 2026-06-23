<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.17`](#kibana81917)
-	[`kibana:9.3.6`](#kibana936)
-	[`kibana:9.4.2`](#kibana942)

## `kibana:8.19.17`

```console
$ docker pull kibana@sha256:1f26170a28367301e33ff66f802a51bf40061a12f44d4910e1b94e9a212821d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.17` - linux; amd64

```console
$ docker pull kibana@sha256:9da486ad3631563c34fb12d6208102614fe44f82d4e7283b30bf4b89a5da065e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.4 MB (455446566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c8b366b756a0068cb279ed7f8c674d5aa268a21eda498fad11197e8cd6d862`
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
# Tue, 23 Jun 2026 18:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 23 Jun 2026 18:49:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 18:57:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 23 Jun 2026 18:57:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:57:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 23 Jun 2026 18:57:36 GMT
RUN fc-cache -v # buildkit
# Tue, 23 Jun 2026 18:57:36 GMT
WORKDIR /usr/share/kibana
# Tue, 23 Jun 2026 18:57:36 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 23 Jun 2026 18:57:36 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:57:36 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:57:36 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 23 Jun 2026 18:57:36 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:57:37 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 23 Jun 2026 18:57:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 23 Jun 2026 18:57:38 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 23 Jun 2026 18:57:38 GMT
LABEL org.label-schema.build-date=2026-06-18T10:19:39.732Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a951847dc9bf6f747f1cd9f8445c4fc10ce85d40 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.17 org.opencontainers.image.created=2026-06-18T10:19:39.732Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a951847dc9bf6f747f1cd9f8445c4fc10ce85d40 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.17
# Tue, 23 Jun 2026 18:57:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 23 Jun 2026 18:57:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 23 Jun 2026 18:57:38 GMT
USER 1000
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa25ab2eaae43d555996d13545fb8ab419f3424d15017c2cce7c71b1a8ff7d3`  
		Last Modified: Tue, 23 Jun 2026 18:58:38 GMT  
		Size: 11.8 MB (11799967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2a1282fc03d99871ac10c2c23917c15ff64d7c9c46944189ec88a8532a65e6`  
		Last Modified: Tue, 23 Jun 2026 18:58:45 GMT  
		Size: 397.3 MB (397269790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0396cbc2250d8e712754f04587c5991ef839113c840e849cf8291d836ebaa755`  
		Last Modified: Tue, 23 Jun 2026 18:58:37 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150c4a8153d8fba13b337afb777c8549a6a4e9fa43e40125c32b029001b445f4`  
		Last Modified: Tue, 23 Jun 2026 18:58:38 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3553465773b796d50a3768cccee7d707f2674cba3f6fea1906e9104ad9dcace`  
		Last Modified: Tue, 23 Jun 2026 18:58:38 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba241d0512d1e3bf14e3bc0d6c8b2e099cc079f8f028353028cfa20f3c05324`  
		Last Modified: Tue, 23 Jun 2026 18:58:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f200902db65d8a3f7e245f81ffbf5449671acac6b2eb3aecd9ff9fb976f834e`  
		Last Modified: Tue, 23 Jun 2026 18:58:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991f875f058b174dc009e7b88a480790e718901ec0b27221cdd8ccb2c28564a`  
		Last Modified: Tue, 23 Jun 2026 18:58:40 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f87819aac9498c0bd72a3db033b3177a261bc790ef15965a9631d4e32b0793`  
		Last Modified: Tue, 23 Jun 2026 18:58:41 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f337b98ef513010cc33312a721c03fa57004134359c28fe6cb2d55c5b6824c1`  
		Last Modified: Tue, 23 Jun 2026 18:58:41 GMT  
		Size: 161.7 KB (161745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3ea5927d91dd162b8c4233ca0c8cb358eff5f11e0c53c9c4c6158590f4fd9b`  
		Last Modified: Tue, 23 Jun 2026 18:58:41 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.17` - unknown; unknown

```console
$ docker pull kibana@sha256:e40198a1f446943c4dcea6df622fdd6d0b94400e53b813db043268def92ec2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8377b5f8ed71022184e36c41f0ca5d3a2d844cd25ba04039be3d582a72771780`

```dockerfile
```

-	Layers:
	-	`sha256:8b9ab09632d9a8cd83f1d5595b729919791a85ab0b0c1c38747ee4a0e0a0ee76`  
		Last Modified: Tue, 23 Jun 2026 18:58:37 GMT  
		Size: 5.0 MB (4955613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7703ae14bf06f98c1439e8559cabd40f2b0ea2823b39dfc50f57da5db336c2`  
		Last Modified: Tue, 23 Jun 2026 18:58:37 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.17` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8549319aabd849fbe21bce8f1d956508316ed4d995850d44e187b2ff290e9ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.2 MB (467177224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47693b87f59bcb5c1f4e226e32ff3eff100501e00af2f8b8fb50701db6a51ee`
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
# Tue, 23 Jun 2026 18:48:32 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 23 Jun 2026 18:48:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 18:55:23 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 23 Jun 2026 18:55:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:55:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 23 Jun 2026 18:55:24 GMT
RUN fc-cache -v # buildkit
# Tue, 23 Jun 2026 18:55:24 GMT
WORKDIR /usr/share/kibana
# Tue, 23 Jun 2026 18:55:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 23 Jun 2026 18:55:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:55:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:55:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 23 Jun 2026 18:55:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:55:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 23 Jun 2026 18:55:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 23 Jun 2026 18:55:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 23 Jun 2026 18:55:26 GMT
LABEL org.label-schema.build-date=2026-06-18T10:19:39.732Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a951847dc9bf6f747f1cd9f8445c4fc10ce85d40 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.17 org.opencontainers.image.created=2026-06-18T10:19:39.732Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a951847dc9bf6f747f1cd9f8445c4fc10ce85d40 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.17
# Tue, 23 Jun 2026 18:55:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 23 Jun 2026 18:55:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 23 Jun 2026 18:55:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ee12d0b395461e82cd4e28f76c7edc2e44e9606214dcc8c41f733e8f65191`  
		Last Modified: Tue, 23 Jun 2026 18:56:33 GMT  
		Size: 11.6 MB (11632894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd01ebc1f87261814822bb326d3eafe67b9519ce284e2815c21b4754203209b`  
		Last Modified: Tue, 23 Jun 2026 18:56:42 GMT  
		Size: 410.0 MB (410027813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f4701976fdce02a7d492b5af61c274b354b6b915de80b96fed2ccca03be19c`  
		Last Modified: Tue, 23 Jun 2026 18:56:32 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f31769d1b2f5229d5e21a554a9f87159fbcf76523ce907e78170b32c7effa32`  
		Last Modified: Tue, 23 Jun 2026 18:56:33 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc57c8676d0e92268067a1ba57e974305b7f2dcd8ebf16e1205f5268f3020753`  
		Last Modified: Tue, 23 Jun 2026 18:56:34 GMT  
		Size: 5.2 KB (5248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8734e702ca2fc4f047e5b164d22c63155d2dad4f9c0e353ce5d0b8bc4398d`  
		Last Modified: Tue, 23 Jun 2026 18:56:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f184d13c6c95db2a94a26ceea0be43cadca8cc9531bc257abb3f843fab4b1c`  
		Last Modified: Tue, 23 Jun 2026 18:56:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cd1092ec461660127561692619e1d1dffee0da9317a68c1d538fcca5ce4ee2`  
		Last Modified: Tue, 23 Jun 2026 18:56:35 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30e563d588fbc2739b85b21855672ddfe296a9f0a31a730b848d6a14581406`  
		Last Modified: Tue, 23 Jun 2026 18:56:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c88dfe1e03ea15663ecc9d458656c729268dc00cc26a6ebe83491542b35b5d`  
		Last Modified: Tue, 23 Jun 2026 18:56:36 GMT  
		Size: 158.3 KB (158261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfe021673e3b1bc1423fa2b5754dabbb67f7d630a0a0f46758231937b3b43ad`  
		Last Modified: Tue, 23 Jun 2026 18:56:37 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.17` - unknown; unknown

```console
$ docker pull kibana@sha256:6803d874f1f66b49288adb3189d07b1500a9c64f8501a0828bf59e0bec374cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4997852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e07cc08220386b1173d2b46115977e3439223be4c66571b5c8874874ac6fb34`

```dockerfile
```

-	Layers:
	-	`sha256:f79193528791081934213aeaba851f594b4327086775c10574f6133192e02de0`  
		Last Modified: Tue, 23 Jun 2026 18:56:33 GMT  
		Size: 5.0 MB (4956677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaae5ed92a58382ca6dc6681994b17779ac2e6e32695ec6b336ee1d34ea313cc`  
		Last Modified: Tue, 23 Jun 2026 18:56:32 GMT  
		Size: 41.2 KB (41175 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.6`

```console
$ docker pull kibana@sha256:bf388ef85a5f1b38050cf9e721a716deefd61cd54c7c33152cd3be7e2521bca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.6` - linux; amd64

```console
$ docker pull kibana@sha256:1feaeaaf38d29908cbcfe566e321708d779777c3c3716eb6ef663608a52de7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464645233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89a22d0c7b5372fe3a8669b5a62f2ad6c16f1ac414ed24f29839b2c65e6ca94`
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
# Tue, 23 Jun 2026 18:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 23 Jun 2026 18:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 23 Jun 2026 18:55:36 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 23 Jun 2026 18:55:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:55:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 23 Jun 2026 18:55:36 GMT
RUN fc-cache -v # buildkit
# Tue, 23 Jun 2026 18:55:36 GMT
WORKDIR /usr/share/kibana
# Tue, 23 Jun 2026 18:55:37 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 23 Jun 2026 18:55:37 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:55:37 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:55:37 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 23 Jun 2026 18:55:37 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:55:37 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 23 Jun 2026 18:55:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 23 Jun 2026 18:55:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 23 Jun 2026 18:55:38 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 23 Jun 2026 18:55:38 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 23 Jun 2026 18:55:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 23 Jun 2026 18:55:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 23 Jun 2026 18:55:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 23 Jun 2026 18:55:38 GMT
USER 1000
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59e8a742fdd28057fde2bb42918f1a4b6ff5a736eaafab5220bbe65e2b4e90b`  
		Last Modified: Tue, 23 Jun 2026 18:56:41 GMT  
		Size: 19.3 MB (19331661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231044e54e241b90c0e00702d8f1da623bcf5d13d1dbdf7b40a7af9e54583380`  
		Last Modified: Tue, 23 Jun 2026 18:56:51 GMT  
		Size: 388.1 MB (388074947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1106b2b0f094607abbb2c223cd17e4c30a105a80a67a6245101c6750f986c4`  
		Last Modified: Tue, 23 Jun 2026 18:56:39 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc49ef2551ee1341e87ef671adf9bdf40a9d94974fefe13329465b6e2e12a8f`  
		Last Modified: Tue, 23 Jun 2026 18:56:41 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1ef6e7a990d6e744bbc9fe87ab917ad8049a3b4d32b55cae515afa846ce8a`  
		Last Modified: Tue, 23 Jun 2026 18:56:41 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6199a7cc653150f3532773dcf02d79b24f8fca203d03fe8d5ee7aff975ac43`  
		Last Modified: Tue, 23 Jun 2026 18:56:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a48dcaba9054ab7f48f394bfd75982d9883696e143b6bf7cf86831003706237`  
		Last Modified: Tue, 23 Jun 2026 18:56:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5736cd29e1fdf0e4789908f826c86963308da2b2914e785319ba5fef765c99ad`  
		Last Modified: Tue, 23 Jun 2026 18:56:42 GMT  
		Size: 4.9 KB (4930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7955abe12a438bc557d76197c89bdabeb8d7ce81fdc2cf48ac0c8e2d21798303`  
		Last Modified: Tue, 23 Jun 2026 18:56:44 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad95a533803fea9dd7d355361bb493106bbc12b2d4fe3926b13bb84c6168e56`  
		Last Modified: Tue, 23 Jun 2026 18:56:44 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e143e77222dea4e2283aece702e66dbf09b3e6848227e25c718292d0611ad9`  
		Last Modified: Tue, 23 Jun 2026 18:56:44 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bebc682165c6dee3e3282e4b5cd463ccddd229a7dbf908b8aa31bff71599965`  
		Last Modified: Tue, 23 Jun 2026 18:56:45 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:19f2c2ed4532de33cbe3010e2fcc91e6bde0bf2e805e1e975ca8f638b757694a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269cb3cc836881dbcd148ded9f79d7af3bbc6f069fa971ef15b68ce331825d23`

```dockerfile
```

-	Layers:
	-	`sha256:853352238e776c9a3d6046fdd7e29908c428b477d6959a24cd086a40c8f970e5`  
		Last Modified: Tue, 23 Jun 2026 18:56:40 GMT  
		Size: 5.8 MB (5812833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506a572becadde29ff939ba2aed3e8fe779846147c957359218fc7b3a3ad7bdf`  
		Last Modified: Tue, 23 Jun 2026 18:56:39 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:73bfda7d7f45bd0963c93c3b13d7480e6d7f4d9eae42a08ece9bac6dc2f56ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.6 MB (475556704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf4c1e52983ebe2fa8a1eac9f2f1299377aa822bd9e0b9d0cace14470a7bf6d`
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
# Tue, 23 Jun 2026 18:49:18 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 23 Jun 2026 18:49:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 23 Jun 2026 18:55:51 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 23 Jun 2026 18:55:52 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 23 Jun 2026 18:55:52 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 23 Jun 2026 18:55:52 GMT
RUN fc-cache -v # buildkit
# Tue, 23 Jun 2026 18:55:52 GMT
WORKDIR /usr/share/kibana
# Tue, 23 Jun 2026 18:55:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 23 Jun 2026 18:55:52 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 23 Jun 2026 18:55:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jun 2026 18:55:52 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 23 Jun 2026 18:55:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 23 Jun 2026 18:55:53 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 23 Jun 2026 18:55:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 23 Jun 2026 18:55:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 23 Jun 2026 18:55:54 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 23 Jun 2026 18:55:54 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 23 Jun 2026 18:55:54 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 23 Jun 2026 18:55:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 23 Jun 2026 18:55:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 23 Jun 2026 18:55:54 GMT
USER 1000
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab466be574546e5c5dd1bf2d4787569305e3b94a93a42ec32732945cbd67a76`  
		Last Modified: Tue, 23 Jun 2026 18:57:01 GMT  
		Size: 19.3 MB (19291989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e11fb445d2eebe035ab08653ab132db41439020c0ea6f3f0477f204bb8ac75d`  
		Last Modified: Tue, 23 Jun 2026 18:57:16 GMT  
		Size: 400.8 MB (400834784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333931af217b0b90277702a4c4e1e1fd090ed7a66b0aa67dcae197adfb02ed27`  
		Last Modified: Tue, 23 Jun 2026 18:57:00 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d3510f968bda0c5a29654be977ef56408a6bb68d916dd0e4ba136c2305f7ed`  
		Last Modified: Tue, 23 Jun 2026 18:57:01 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540995dfe692d21f7fcef2129cff798c5459007a2f10c1c8795394d0f0d14fcf`  
		Last Modified: Tue, 23 Jun 2026 18:57:01 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11d76a7488e8e52f4bdf0bb83c501fd1fdbf8f8632253ef882e9c6540ee2dfc`  
		Last Modified: Tue, 23 Jun 2026 18:57:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be4c6e6a93a48bfe3680a5def9195f784e6b155fe7a2a7ca0fe250c66b37f13`  
		Last Modified: Tue, 23 Jun 2026 18:57:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a133f9dd9ca72b93920e4631f8e7cd554cb93b7fcd6bb7462d709739ca064117`  
		Last Modified: Tue, 23 Jun 2026 18:57:03 GMT  
		Size: 4.9 KB (4928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e63222274d9a0a2818b11a507a88a8ced04fdee1275a9afe269b00bc08886`  
		Last Modified: Tue, 23 Jun 2026 18:57:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1310dbda869aa9532cd03ae7224d36d5d39e7dca1b4e1d6feda36eac2717315`  
		Last Modified: Tue, 23 Jun 2026 18:57:04 GMT  
		Size: 73.5 KB (73455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23034556d6028f87bf6507cc52b9aab7599df0890864aa82785c14a646890a81`  
		Last Modified: Tue, 23 Jun 2026 18:57:04 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c880549fae05bf835aae9ca6020578ed992f742b841b8d937b6e55764540e3b`  
		Last Modified: Tue, 23 Jun 2026 18:57:06 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:bd41aa8b3d8f120e5b58bc76cd0036a92aadf7639f1d506b27ffaa89282f2830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b815be12b961e4bae27daa9951e08a6bc048c96925e797ac4d7aceabd4616905`

```dockerfile
```

-	Layers:
	-	`sha256:40377e42c5e392250af26f61886ad31ff61b3a053af9bfb035437909e1b1ec5e`  
		Last Modified: Tue, 23 Jun 2026 18:57:00 GMT  
		Size: 5.8 MB (5811505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d196a4e5497152fba1f889e42158aee88c79c74f9d57c4addcdc028e754bad7f`  
		Last Modified: Tue, 23 Jun 2026 18:57:00 GMT  
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
