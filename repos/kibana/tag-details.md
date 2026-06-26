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
$ docker pull kibana@sha256:160e7c2bceb8d276c9cbda3d4000c4c7043b1016afac83d2cdfd48eb59b11921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.6` - linux; amd64

```console
$ docker pull kibana@sha256:888fc1be481f4e45b0eb87921da8085f1890623e02fd9c14fb817441035bcd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464642166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821b2f95c757b7cb0e3c5adfc08a5c028a4c89ddfe1c796dd2ebd33965c066d5`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:27:32 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 25 Jun 2026 23:27:32 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
RUN fc-cache -v # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
WORKDIR /usr/share/kibana
# Thu, 25 Jun 2026 23:35:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:35:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:35:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 25 Jun 2026 23:35:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:35:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 25 Jun 2026 23:35:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 25 Jun 2026 23:35:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 25 Jun 2026 23:35:29 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Thu, 25 Jun 2026 23:35:29 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 25 Jun 2026 23:35:29 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:35:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 25 Jun 2026 23:35:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 25 Jun 2026 23:35:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879c6d1c0b7c619457548ba35562680ff8cb9450678d66020d10d9c5c5c04d9f`  
		Last Modified: Thu, 25 Jun 2026 23:36:27 GMT  
		Size: 19.3 MB (19330854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f96807a10f8a0be342627c475fec231bd9e6d566fbe2dd13576549b0cde2a84`  
		Last Modified: Thu, 25 Jun 2026 23:36:35 GMT  
		Size: 388.1 MB (388063625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e8aa4706959a2dbf6b897233bf48a35cdb6842d6d6a33556a5800b8510f2fa`  
		Last Modified: Thu, 25 Jun 2026 23:36:26 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c837c4c80a6686a8ef8661b34a79070ab6d567050ac0b5b927f1c8fd7833f2`  
		Last Modified: Thu, 25 Jun 2026 23:36:27 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f11d2564cd44f687c23bcc825b208e04de95e6a8acee776709f69c78d9510c`  
		Last Modified: Thu, 25 Jun 2026 23:36:27 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456008b35fe12cd5d93305e81cf960e8b2f96328bcdb51598c6a45ccc5a69e45`  
		Last Modified: Thu, 25 Jun 2026 23:36:29 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c59cf1e6e98e498620827df73b2fb161beb49c5e246d52323a77195b03becb9`  
		Last Modified: Thu, 25 Jun 2026 23:36:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ec18e76fed13fa23e2ecfdc7ca0c5f6236e9c8262bd1f811a55c8b7420ff7`  
		Last Modified: Thu, 25 Jun 2026 23:36:29 GMT  
		Size: 4.9 KB (4928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc03ada75af6df4aa934d3a8fdae91fbb846cd9d585e987196f2f67025fa9e3`  
		Last Modified: Thu, 25 Jun 2026 23:36:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4284c21f050a8afec88521fb77dc8aa46a284b851fae4450d66a447411c27512`  
		Last Modified: Thu, 25 Jun 2026 23:36:30 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6fa62b7a2cb677677a02f2ccb79df499744da42541a4f8e666e235ff1c2cf4`  
		Last Modified: Thu, 25 Jun 2026 23:36:30 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b9b052e1aebfb26b2105cb0137a955dbc1d76bd89bf05af1fc0feb545cfac`  
		Last Modified: Thu, 25 Jun 2026 23:36:31 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:326b88169e0e0373c25653ea218df6bcf61577cddce508d763b868dd3292c3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e760871efa964cbf83072bde760b0773a5860164524bf7a9118865e8a25e4a`

```dockerfile
```

-	Layers:
	-	`sha256:b0ba30b792a5b9c1a2c875c355875301bdf0cf8fa0c480745a1305f0fea672ea`  
		Last Modified: Thu, 25 Jun 2026 23:36:26 GMT  
		Size: 5.8 MB (5812863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e93c521f91823390fcb43a785036d08c6589abdf66263b522bfb1c6dad0210`  
		Last Modified: Thu, 25 Jun 2026 23:36:26 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e0b68146f62bbb07004197769993cc8f5f963dce36637b68e9467f97ac716547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.5 MB (475491533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6098a003855cab3153a46f00d046a87e9ee5478c25268e66beab84475d42257`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:42 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 25 Jun 2026 23:26:42 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:33:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 25 Jun 2026 23:33:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:33:14 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 25 Jun 2026 23:33:14 GMT
RUN fc-cache -v # buildkit
# Thu, 25 Jun 2026 23:33:14 GMT
WORKDIR /usr/share/kibana
# Thu, 25 Jun 2026 23:33:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 25 Jun 2026 23:33:14 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:33:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:33:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 25 Jun 2026 23:33:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:33:15 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 25 Jun 2026 23:33:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 25 Jun 2026 23:33:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 25 Jun 2026 23:33:16 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Thu, 25 Jun 2026 23:33:16 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 25 Jun 2026 23:33:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:33:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 25 Jun 2026 23:33:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 25 Jun 2026 23:33:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ad5aa2aac3987ab100ebbeaaa3882eb1781d0c3676539db19a69f909a68b6d`  
		Last Modified: Thu, 25 Jun 2026 23:34:23 GMT  
		Size: 19.3 MB (19283308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5c60d989dec319e4619d741e77377ba116f00e0ded955e5a46de4635fdd3f9`  
		Last Modified: Thu, 25 Jun 2026 23:34:30 GMT  
		Size: 400.8 MB (400833228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958f294146c35127575b0f419bc2447b0bda829bb869e3321490162b5767912a`  
		Last Modified: Thu, 25 Jun 2026 23:34:21 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e11a39cc52c3d2c05951fd6503014f388ec1c9e0030e8b8bd3ae5b1ae7b697c`  
		Last Modified: Thu, 25 Jun 2026 23:34:22 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce553b4675ab5aa2c25659aa1d742a944b65d402840f73e96dce5186ea1c8f5`  
		Last Modified: Thu, 25 Jun 2026 23:34:22 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3a1f7e87efd6071bd53198e42a8d665d71c19b61b37b46b5ae17c320716191`  
		Last Modified: Thu, 25 Jun 2026 23:34:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452c440a18ae5dbb70580209ca1a04a32c8cd144c0a7bda0f4ace56aed1fc774`  
		Last Modified: Thu, 25 Jun 2026 23:34:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c892e6733a160e141daf95011aec84603429d7156ec6d068c7451ed723340c`  
		Last Modified: Thu, 25 Jun 2026 23:34:24 GMT  
		Size: 4.9 KB (4928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb550410870873961cbc20ed8073d5f5657e7f4e6ebf5c5ccfccab8ff611a4`  
		Last Modified: Thu, 25 Jun 2026 23:34:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e088cf26117870fc0ecead2059812b33e196f82232c147a8266909a0c131461`  
		Last Modified: Thu, 25 Jun 2026 23:34:25 GMT  
		Size: 73.5 KB (73452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1967aae28355190478f1a465f23674f9526f27720526cc758a16cd50f5450070`  
		Last Modified: Thu, 25 Jun 2026 23:34:26 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4dc8a26f45af9e919e2bf3a2527e0dd7abca35b93bea8a33c413813b0d039b8`  
		Last Modified: Thu, 25 Jun 2026 23:34:26 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:5e43f9ad91c04bf8cd20888434129f03a092f67fa92b8e2a74e3bf9cf2ea7385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5853236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7c49dba8c6fbf329e6a51f635926e03a80c6965defbb7d9c220db68a0bbd28`

```dockerfile
```

-	Layers:
	-	`sha256:777f4842d07219d6b4c4d8383394d2353874b0b80c0537cb0167d1186868fa72`  
		Last Modified: Thu, 25 Jun 2026 23:34:22 GMT  
		Size: 5.8 MB (5809753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c39b836908db641037c9e36492eed1362ba631ff6c0ea1a8be3d51711436f2`  
		Last Modified: Thu, 25 Jun 2026 23:34:21 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.2`

```console
$ docker pull kibana@sha256:90b9ef031ca1d1a9a10e0442d075e1c4a060db47e3a0f20eda3a24caa98fec26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:c47b446b3808d84f2ba1e84458be0cdcc3432ae3be022d286074dd79a21dd761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535327667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e0ae47921d3d6809ee3c3f9db33acd4b2b004273531bf615057c3f08d02ab6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:27:34 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 25 Jun 2026 23:27:34 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:34:58 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 25 Jun 2026 23:34:59 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:34:59 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 25 Jun 2026 23:34:59 GMT
RUN fc-cache -v # buildkit
# Thu, 25 Jun 2026 23:34:59 GMT
WORKDIR /usr/share/kibana
# Thu, 25 Jun 2026 23:34:59 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 25 Jun 2026 23:34:59 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:34:59 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:34:59 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 25 Jun 2026 23:34:59 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:35:00 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 25 Jun 2026 23:35:01 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 25 Jun 2026 23:35:01 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 25 Jun 2026 23:35:01 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 25 Jun 2026 23:35:01 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 25 Jun 2026 23:35:01 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:35:01 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 25 Jun 2026 23:35:01 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 25 Jun 2026 23:35:01 GMT
USER 1000
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734c560cd7c6eb8de08909cb0e15a9f1f61a4ca88d2b2f70b71ef0d7de0c42e6`  
		Last Modified: Thu, 25 Jun 2026 23:36:11 GMT  
		Size: 19.3 MB (19330878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffc35c8033ffc47915f933eb41fdf5121c04b8b67d7d92e33b3dc7a1f229c6`  
		Last Modified: Thu, 25 Jun 2026 23:36:21 GMT  
		Size: 458.7 MB (458749110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32512be5e5d95c6bb9b42cfe9d9a342d55f4e23df32323309186276b7fbd43c`  
		Last Modified: Thu, 25 Jun 2026 23:36:09 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0142504c94e0cf07184e1dbf7bfd58e2ed15bddde7cfd2ede461e119b9f4c50`  
		Last Modified: Thu, 25 Jun 2026 23:36:10 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584e6f1984f2db6d59e2e46f6c04ee6c91d78ea1370f96c901324e6deb045e61`  
		Last Modified: Thu, 25 Jun 2026 23:36:11 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bb8e8f3bad1ace7da4cc0b496c4c13a6dc144d4d23df9c6e2cb495a9f9d6de`  
		Last Modified: Thu, 25 Jun 2026 23:36:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bec2ce4bd18a0e2ba701f41806e3a9046685575d78c62aab1fd9e9680f495d`  
		Last Modified: Thu, 25 Jun 2026 23:36:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715ca794f534393e0cb509bbc0f4cfa175a40636661055edfe8a22bbcb8ad150`  
		Last Modified: Thu, 25 Jun 2026 23:36:13 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33589a1b7e4c740aaa0b05d03287baaee7bd20cc74838fd7d09020033ad7a416`  
		Last Modified: Thu, 25 Jun 2026 23:36:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf53ec5af410fc5d2b18991459b417dc018a78cd25456349a5f89364428864e8`  
		Last Modified: Thu, 25 Jun 2026 23:36:14 GMT  
		Size: 74.5 KB (74543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1a8704b6d6968252f37fe54df560485cbf2d8860cab2d8a2a1a88bd9d1035b`  
		Last Modified: Thu, 25 Jun 2026 23:36:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0853e56cd5d34ff240ac8e46c9d0873392b90cdee545e4ff7adbac3d160271e1`  
		Last Modified: Thu, 25 Jun 2026 23:36:15 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:dfdc095a72867407152277ad86df0832d7a0d22a8eee55ffc087bec1f27371d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2389f0bc69773e46123af1169f93fb7ef5251105b304c6fa3e9cf6e01b38410c`

```dockerfile
```

-	Layers:
	-	`sha256:b6f2881c74de6932c89ecb00e9bee2d844a9d405a4088c392b4c9b3bc4ed9e77`  
		Last Modified: Thu, 25 Jun 2026 23:36:10 GMT  
		Size: 6.0 MB (6021133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2329c96530eca203ecbb7c5c2d64b5fbfe6c3b2e62c5291d36abf5b4e8277e4f`  
		Last Modified: Thu, 25 Jun 2026 23:36:09 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d5036d89b9d7e476639884486ed6c26fe5e20c957d72e091bcc0702b33884128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546273748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a1fd250475409b26283efe6c1a4aa8719bb92fcd4045a43394cadb8f47390e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:42 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 25 Jun 2026 23:26:42 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:34:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 25 Jun 2026 23:34:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 25 Jun 2026 23:34:48 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 25 Jun 2026 23:34:48 GMT
RUN fc-cache -v # buildkit
# Thu, 25 Jun 2026 23:34:49 GMT
WORKDIR /usr/share/kibana
# Thu, 25 Jun 2026 23:34:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 25 Jun 2026 23:34:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 25 Jun 2026 23:34:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:34:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 25 Jun 2026 23:34:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 23:34:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 25 Jun 2026 23:34:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 25 Jun 2026 23:34:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 25 Jun 2026 23:34:51 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Thu, 25 Jun 2026 23:34:51 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 25 Jun 2026 23:34:51 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 25 Jun 2026 23:34:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 25 Jun 2026 23:34:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 25 Jun 2026 23:34:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06efb77ff3c13d1fe87b8c3a470da44efc267542a4bbf862fa754d8c8516043`  
		Last Modified: Thu, 25 Jun 2026 23:36:12 GMT  
		Size: 19.3 MB (19283240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8098a6e825f9708b09c9fd95f6162d85a79a700c96485bb978426f7603765686`  
		Last Modified: Thu, 25 Jun 2026 23:36:21 GMT  
		Size: 471.6 MB (471615500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583ea31e6a5f915bab6a949de28ef8e12c36d3f4c67741c697bb9dcb5d47807`  
		Last Modified: Thu, 25 Jun 2026 23:36:10 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f75d8290c1f7b57903801b8d6fd4db815edd27deeba63cf8bb297c15da4834`  
		Last Modified: Thu, 25 Jun 2026 23:36:12 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06bef19f7873ef465aae302166ff8a4166be914e38b69f1ac6e8d4011c2368b`  
		Last Modified: Thu, 25 Jun 2026 23:36:12 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89778028c1a7c9a1ae85fa2231a436998b7172566a36732b56ff4ef9f58b8208`  
		Last Modified: Thu, 25 Jun 2026 23:36:13 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42923f3c8134cc8f1c2c039ad06b3c631855664d84362fb89c8ea7a0c962372e`  
		Last Modified: Thu, 25 Jun 2026 23:36:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4ed06f834f00b866c81f64c4a0997b8d4c5e6f024c8733f19c6a9c6d7bd7e7`  
		Last Modified: Thu, 25 Jun 2026 23:36:13 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87738391e965b7b945f2f353ec3e90594ec7e923cd0ba91143b7c9e606966bb1`  
		Last Modified: Thu, 25 Jun 2026 23:36:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32d511f114be6ff40bcf06b730ef6f340b945efe4c93815fa9c410a2efc61f6`  
		Last Modified: Thu, 25 Jun 2026 23:36:15 GMT  
		Size: 73.5 KB (73451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d1aa5702e454fa543b3b667d2a2299192115851b03c8bf4a9422d3f6de8521`  
		Last Modified: Thu, 25 Jun 2026 23:36:15 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bf253a02b82ba236351d1dfb8a3190cc33f27d0bf7c54d4f02d5043738c32d`  
		Last Modified: Thu, 25 Jun 2026 23:36:16 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:7d40996ff5ed2c15eb01cfa93445bdb29b0f3b6e673bc820ca741bfeb3f60626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6061506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e471f7792eac64ccbebaf4dba0164913862b57571cc03532a337f0c105cab1bd`

```dockerfile
```

-	Layers:
	-	`sha256:d50ee6e4bd918607e9c29a4b7cbed77f717537cad575518f09efc7ca58da6b42`  
		Last Modified: Thu, 25 Jun 2026 23:36:11 GMT  
		Size: 6.0 MB (6018023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa6700e86f0d814f105d9a2ef3ae4ed942242d122ec32073fc664c3867df3ab`  
		Last Modified: Thu, 25 Jun 2026 23:36:10 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
