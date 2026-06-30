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
$ docker pull kibana@sha256:bded3d3e1569cf2755af9a6813fa54a46748d9aed1e8aa1bab9a81bb394379a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.6` - linux; amd64

```console
$ docker pull kibana@sha256:96b21174b6c08568abfa459480cd4079e734db3c1be4de5e399532bb304b2fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464646635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7af8441b8cacbcd8fade7a785d89e3a9589d11270d0901cd103d82bee4b676`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:12:27 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 00:12:27 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:21:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 00:21:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:21:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 00:21:12 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 00:21:12 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 00:21:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 00:21:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:21:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:21:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 00:21:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:21:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 00:21:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 00:21:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 00:21:14 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 30 Jun 2026 00:21:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 00:21:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:21:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 00:21:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 00:21:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8001f4eeada368ed0a7fca9ff9414919f93b22d79d27738ad1f4b03d1ab421e2`  
		Last Modified: Tue, 30 Jun 2026 00:22:16 GMT  
		Size: 19.3 MB (19331505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c61442ceaa68b9c2273a90c75dbe3b6eb5f57605845466b50c5bc05f76fb64`  
		Last Modified: Tue, 30 Jun 2026 00:22:25 GMT  
		Size: 388.1 MB (388069883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b3fd5abd6f4ded9f106ec9cef0bec3f6980f4743600c0a333fb802e22b9192`  
		Last Modified: Tue, 30 Jun 2026 00:22:15 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c53a23ab3e98c6fd1f077e4e98dcc516f00815053fb2bdaa5550be2973219`  
		Last Modified: Tue, 30 Jun 2026 00:22:16 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925fe1f4549603f6c7caa56fb18adbd0bad39e22f52b94f5d2aa31265504ad9`  
		Last Modified: Tue, 30 Jun 2026 00:22:16 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8679bb4164b20bdec5617a254c66f9c6b02c548823139b3e3ba3fdd3b6e51de9`  
		Last Modified: Tue, 30 Jun 2026 00:22:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed401222ec3c65c149370823df4209a9bdddb161a032de8ea72d58c3cd747f`  
		Last Modified: Tue, 30 Jun 2026 00:22:18 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465024f5f3cc376d8e918ef0583672f322ca0fd79491b7d6530640f1a3a16347`  
		Last Modified: Tue, 30 Jun 2026 00:22:19 GMT  
		Size: 4.9 KB (4926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037c9771fa9a5a6a42ddcfdcc06dc6e0588fee92ff20e8a75ada50eb0604c6af`  
		Last Modified: Tue, 30 Jun 2026 00:22:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed04727846e95bbfc68c4b87efaf6ebdf92a83f49e305536684f313813646438`  
		Last Modified: Tue, 30 Jun 2026 00:22:20 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d729eeb6d6bcd6c9eb64b8b256dfa508aaba14c23577981d2065ef39ba27cd02`  
		Last Modified: Tue, 30 Jun 2026 00:22:20 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed5df8cecef81075b461940098b0dd0a3f34ac428bd5018c0f8b67a44a31bd0`  
		Last Modified: Tue, 30 Jun 2026 00:22:21 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:7fd76be3d11de578191e53951c8323dd3f113d243e05f28e397226976a888459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a559e38b07308597bbe83156eae82fa123b7ae12e7e725ab14a842244693f36`

```dockerfile
```

-	Layers:
	-	`sha256:09586553e26af85abab09125e30f430d1593bf4f70c143f4d527183517d1c817`  
		Last Modified: Tue, 30 Jun 2026 00:22:16 GMT  
		Size: 5.8 MB (5812871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1708f2a7f98c186a779cabcbea860ee3a48c27e0f7f2f36e92c21bb2c76fabb0`  
		Last Modified: Tue, 30 Jun 2026 00:22:15 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6900ebf2fca574d12781631fdd28abe0fc3dd33caa0c9f47f9d34a7bd42f7a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.5 MB (475501032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796775181123529d0c29b2b1dc59246e967d20977d18d9530c930a1032db84c5`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:10:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 00:10:48 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:17:39 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 00:17:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:17:40 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 00:17:40 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 00:17:40 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 00:17:40 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 00:17:40 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:17:40 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:17:40 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 00:17:41 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:17:41 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 00:17:42 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 00:17:43 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 00:17:43 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Tue, 30 Jun 2026 00:17:43 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 00:17:43 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:17:43 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 00:17:43 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 00:17:43 GMT
USER 1000
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b9480ce811dd9300cf2260fe792ee3c74bebfb9752528c5ad78493bec1de13`  
		Last Modified: Tue, 30 Jun 2026 00:18:50 GMT  
		Size: 19.3 MB (19283502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1173f60a8d14f171c8c9d81e828c46ab7429a41a01f18bbab67ffc89d299f7fc`  
		Last Modified: Tue, 30 Jun 2026 00:18:59 GMT  
		Size: 400.8 MB (400841182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ac84ce4c35fc85a4fb6f9f838954361eba2378cfec5ab37a207ad92f1054c2`  
		Last Modified: Tue, 30 Jun 2026 00:18:48 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf7c78429775041465550561a23ade910c683a0165a6218505195d1b940f015`  
		Last Modified: Tue, 30 Jun 2026 00:18:49 GMT  
		Size: 16.5 MB (16460496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff4958d9385a1c06e6528a382f37744076a6b4a1fdb7abeee5c8b97d05a8293`  
		Last Modified: Tue, 30 Jun 2026 00:18:49 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f104a48734ce83ae35e99041cfe1579a27e078e0d5f8ee507f0b7341b072795`  
		Last Modified: Tue, 30 Jun 2026 00:18:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41704132927d741fc6105a0771786c12e274dcec728185b32c6e1bd02fd7f983`  
		Last Modified: Tue, 30 Jun 2026 00:18:51 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724c6e3b907e9dd98ccca51969d28ce92857bcfe1ae251a200401264a3c08d76`  
		Last Modified: Tue, 30 Jun 2026 00:18:52 GMT  
		Size: 4.9 KB (4925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21691bc593461de00a60efde2dd8c277f1f5ef94f3f9e31ca30bf01d89cd8096`  
		Last Modified: Tue, 30 Jun 2026 00:18:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1b9e968235d9a70f090b1a7d6e12799f270d4abdf17da711fe0474f0d1ba3e`  
		Last Modified: Tue, 30 Jun 2026 00:18:52 GMT  
		Size: 73.5 KB (73451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b7ca4ec80fb2d2c417366f50d66d6e00510f786769307edb4c6ba26e37d32`  
		Last Modified: Tue, 30 Jun 2026 00:18:53 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165db568a1339a81b78158bd800cc958d318fed3a02c5ab45b3c0002f2732f68`  
		Last Modified: Tue, 30 Jun 2026 00:18:54 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:29456fb0410de6907c20a39f20aeb47dc96e6748acab7fef4e5055e3c58d5345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5853244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f3ca8fc32a8188fff3f2273b540c65c3daeffedd6fce0b9c02088b2a9bf320`

```dockerfile
```

-	Layers:
	-	`sha256:664d5305210555f84d84a0fd6d92f409edba1058b4bb7db3e2a03f2e90d1e4c6`  
		Last Modified: Tue, 30 Jun 2026 00:18:48 GMT  
		Size: 5.8 MB (5809761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c297bddcb103eb974a7fe4d06eedcaeab95032447eeb796bbed8dae57aeca97`  
		Last Modified: Tue, 30 Jun 2026 00:18:48 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.2`

```console
$ docker pull kibana@sha256:e8d1d7e3798161a70eb5bd875d88829b6c7176d724320c46577ec74b891598a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:596c21beef1563a126ca7ffc9ecb1a7b6132238a6376d2f0fd3d8a9bdf0bb6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535324065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9966fbcd0ce0e1eba5a5fc54c14d3a53759112a4d5b445fb41e0664835f8d47c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:14:25 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 00:14:25 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:24:03 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 00:24:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:24:03 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 00:24:04 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 00:24:04 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 00:24:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 00:24:04 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:24:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:24:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 00:24:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:24:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 00:24:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 00:24:06 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 00:24:06 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 30 Jun 2026 00:24:06 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 00:24:06 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:24:06 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 00:24:06 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 00:24:06 GMT
USER 1000
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7b56ff368c9effc998f54979ccee33e26eed0c53108c99bb5d67d1aaf60762`  
		Last Modified: Tue, 30 Jun 2026 00:25:23 GMT  
		Size: 19.3 MB (19331514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be3e28f3935d33220df5e7312c3674fe4c6ec7fe3deab33ff113ba487c0cdfc`  
		Last Modified: Tue, 30 Jun 2026 00:25:33 GMT  
		Size: 458.7 MB (458747325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9add837ea1b94a750f6ed9319a2d8f1222c1aad5f13be3f4cca135230b566562`  
		Last Modified: Tue, 30 Jun 2026 00:25:22 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b06f4f0963ea278f4874a7da2dbb592f0acb147cc9103927695a28e0645cb1`  
		Last Modified: Tue, 30 Jun 2026 00:25:23 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b6bf66592085fed4aa71dc68590bd5a3fead144dc803b41bc03b217e7508b3`  
		Last Modified: Tue, 30 Jun 2026 00:25:24 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae21b9a816114782b3f0f5ea0329a19f5c3d7c818956a16166c736da527a9318`  
		Last Modified: Tue, 30 Jun 2026 00:25:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc47408de068cef2ff3660050d2516a9db6618c99e5b8b686038954ee81f177`  
		Last Modified: Tue, 30 Jun 2026 00:25:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99abe3a0b86c810b3112ba0059066b5fb87d0351ccb84a92bec5eaa4e8287bc6`  
		Last Modified: Tue, 30 Jun 2026 00:25:25 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ff82475b92bbf0c3c752fd0b231cd43d157eb21b55217aabd16913a0dbe8f9`  
		Last Modified: Tue, 30 Jun 2026 00:25:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd6ad193b5e47c75cdb37aa20de53f36b710653f3e5392862d47dfd7788c18`  
		Last Modified: Tue, 30 Jun 2026 00:25:27 GMT  
		Size: 74.5 KB (74547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96461774497c4778b660a21272fd4b1e704e6ea7a21df98bf9c8e231d80632`  
		Last Modified: Tue, 30 Jun 2026 00:25:27 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaccb62f03493916c9391f44b201c9fcd916e89603fef06f032431100dcc3b1`  
		Last Modified: Tue, 30 Jun 2026 00:25:28 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:178e84cd671f8dd76b0964f761bedb3b606c8c3b252e2225f78879b04c8da0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa1dbd5cdd71a956114bd9dec11b331805e42d2249caec3dcb454036fe88a0c`

```dockerfile
```

-	Layers:
	-	`sha256:8d80432646fa71a858d481169a34bef8afc645a22a840dbf6f622ecc25115952`  
		Last Modified: Tue, 30 Jun 2026 00:25:22 GMT  
		Size: 6.0 MB (6021141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41b19ff27206d5e20636a00b9cfd1ddd4a7a396f438925f57bd92e7117b91de`  
		Last Modified: Tue, 30 Jun 2026 00:25:22 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d0f8159eda9fcb9f40b94df07a676c6ab682a80f830629247e83c835f8dabc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546276909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0805ab39d76e6bc8c22715e879d32c3e988d5bbf424e6ea53f19da1c7aad094e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:12:27 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 00:12:27 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:20:58 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 00:20:59 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 00:20:59 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 00:20:59 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 00:20:59 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 00:21:00 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 00:21:00 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 00:21:00 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:21:00 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 00:21:00 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 00:21:01 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 00:21:02 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 00:21:02 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 00:21:02 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Tue, 30 Jun 2026 00:21:02 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 00:21:02 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 00:21:02 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 00:21:02 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 00:21:02 GMT
USER 1000
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06368861ce88ec24a4ef0ee19b733a87b51a1afc375525f3a399068b094a892`  
		Last Modified: Tue, 30 Jun 2026 00:22:24 GMT  
		Size: 19.3 MB (19283529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e4ad97fe87c1ae267fd7cb60c302cb492aaee2f3bb15ee4c60ae83494e3cc1`  
		Last Modified: Tue, 30 Jun 2026 00:22:36 GMT  
		Size: 471.6 MB (471617038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5d9de2bca5dacbe67ebe028050bed08f437c3cc471eb43c36fcb6927e9acd2`  
		Last Modified: Tue, 30 Jun 2026 00:22:23 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9254740dc8d905a34d7b84e6312f6a511d80a6d8c44c3d0f704982cef6a11a`  
		Last Modified: Tue, 30 Jun 2026 00:22:24 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdf773224f6d553e2b81450cddbef92994707d1d197f340303d57f186a4759c`  
		Last Modified: Tue, 30 Jun 2026 00:22:25 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6372ff681556c1d58257dfb676ca97f1fb2ff4e099acc59210dc9a5cc2beab`  
		Last Modified: Tue, 30 Jun 2026 00:22:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4568ec0e10584380e66c72a33596103d3f3d4dfa2dc60bb433805184a6701b85`  
		Last Modified: Tue, 30 Jun 2026 00:22:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e434de4f046c7a6342eb2d76102193538c94fb6a796f926911d50a39daf937`  
		Last Modified: Tue, 30 Jun 2026 00:22:26 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51a60ebcfa48b473eed9949e5d38c4ef3dee230dc6e6bdfd60267ffaeee8ad4`  
		Last Modified: Tue, 30 Jun 2026 00:22:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1cb33b74fe7e38ad52cb382596a0d8b2bd83888b99c10f17bb2ef3aa85b895`  
		Last Modified: Tue, 30 Jun 2026 00:22:27 GMT  
		Size: 73.5 KB (73452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0cc182dbbe91912055f05eaf786fbeb40cd48bae03687f3a5a07018ee46542`  
		Last Modified: Tue, 30 Jun 2026 00:22:27 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a810a8a853b6716a8c0eced815d17048dc4bf0e914bfc060d9f47a86081a1f`  
		Last Modified: Tue, 30 Jun 2026 00:22:29 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:ea331b25e45ffa181aa7196b84d850d8742ebcc534e0a2d3e701d1ccb592c3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6061514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608a18f91f3aa6d072241302d608cdb13e7c58ec80500148c8a40dd419f970ae`

```dockerfile
```

-	Layers:
	-	`sha256:d4c1c7755a68aa5d9ce7ba74f81ad6ae625588f37860cd76a4d0fb54e009a169`  
		Last Modified: Tue, 30 Jun 2026 00:22:24 GMT  
		Size: 6.0 MB (6018031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b28a280b1886179d231cec6257104c0fbb8f9ed1eb6c6bac1892cd27f7e0519`  
		Last Modified: Tue, 30 Jun 2026 00:22:23 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
