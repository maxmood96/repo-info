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
$ docker pull kibana@sha256:b338cd305b828a0551cf1446928884d82b4fc66a910493f2dd1f507d2cc1acb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.6` - linux; amd64

```console
$ docker pull kibana@sha256:c77c52bf29b8b39865b76dc399215d5c9d7f3c47235634a55b783c00aae58eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.6 MB (464632889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c377ee2d9892a17cb9a4c7c3013f2868b836521c5fb4d74d87748d922474e813`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:58 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 24 Jun 2026 23:04:58 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:11:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 24 Jun 2026 23:11:48 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:11:49 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 24 Jun 2026 23:11:49 GMT
RUN fc-cache -v # buildkit
# Wed, 24 Jun 2026 23:11:49 GMT
WORKDIR /usr/share/kibana
# Wed, 24 Jun 2026 23:11:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 24 Jun 2026 23:11:49 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:11:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:11:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 24 Jun 2026 23:11:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:11:49 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 24 Jun 2026 23:11:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 24 Jun 2026 23:11:50 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 24 Jun 2026 23:11:50 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Wed, 24 Jun 2026 23:11:50 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 24 Jun 2026 23:11:50 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:11:50 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 24 Jun 2026 23:11:50 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 24 Jun 2026 23:11:50 GMT
USER 1000
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c022c8c8210a1bffd91022d16f55f277778350b22dadc6153f06854f4967292`  
		Last Modified: Wed, 24 Jun 2026 23:12:52 GMT  
		Size: 19.3 MB (19331157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb8398b10ba6ccdcacd2a92af50025df42d5fb2423da0caa53e73ea09bd0db`  
		Last Modified: Wed, 24 Jun 2026 23:13:00 GMT  
		Size: 388.1 MB (388072177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fae8bf7153f80e3c0011a0b9f493c74d3fb88a15a3b06ec6aabd20f85df44f1`  
		Last Modified: Wed, 24 Jun 2026 23:12:51 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0860a2ab123c11e9138a84db86828f72a3f74e380bb16c06413ddcaa770b237`  
		Last Modified: Wed, 24 Jun 2026 23:12:52 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae27097d5234eee4ef1dd6bb6c88ff75a3a4d08f6452bccf6243d1d09780b58e`  
		Last Modified: Wed, 24 Jun 2026 23:12:52 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856e183d9a3998fba3dd9f34e1e87f90a5402f65a5b4e4367d8b2119180c300e`  
		Last Modified: Wed, 24 Jun 2026 23:12:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856c6e1a2aa26b47f56959bf68e2878003c3f08909ebea8b117217baa0f389b8`  
		Last Modified: Wed, 24 Jun 2026 23:12:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e76895b649d295851190f043ba5d7e04968efb8463a055ba66f18d19525ede7`  
		Last Modified: Wed, 24 Jun 2026 23:12:54 GMT  
		Size: 4.9 KB (4927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1da5e986a6133325d065c3ac5d76c6e1cb894f7e1adca29c030f08dda2ec4a`  
		Last Modified: Wed, 24 Jun 2026 23:12:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef94f76de0ecc777c05a9ae20f3455ca23f9d3304283975572784a6a8bb84fce`  
		Last Modified: Wed, 24 Jun 2026 23:12:55 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca6dd648322e337fa0ced616b4d22b77bb910fdc47c388383bba946fdef9e26`  
		Last Modified: Wed, 24 Jun 2026 23:12:55 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdc5c675e54cb5efccb7ed8004f96266c0335a5004801e53a70abe2bc871a0c`  
		Last Modified: Wed, 24 Jun 2026 23:12:56 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:f86335545a297df0b3b9fb7b5115a533db46a8d454696e7ea9256421bb8c8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa03cf792e317ca157499285528b1a27f67710aed46f54aa2670170cbcb7c0b1`

```dockerfile
```

-	Layers:
	-	`sha256:b3b6fb81ef8bb1619122694cbbbb6fbf076e0a231dd4cd73920979f717b0b92d`  
		Last Modified: Wed, 24 Jun 2026 23:12:51 GMT  
		Size: 5.8 MB (5812845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cadb9be9298af1b6fbbb09b4dfa0c590ec8bb01911687bd6df3437573390db0`  
		Last Modified: Wed, 24 Jun 2026 23:12:51 GMT  
		Size: 43.2 KB (43225 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:ce727e07a98f9ec0969e253c772809f1ba6566fabf293eeed9da2a821a09d9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.5 MB (475485532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2657189fbfda7f2bd357e7861d8813258ee607f5951edfd7168053a357028b56`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:11 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 24 Jun 2026 23:04:11 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:11:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 24 Jun 2026 23:11:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:11:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 24 Jun 2026 23:11:57 GMT
RUN fc-cache -v # buildkit
# Wed, 24 Jun 2026 23:11:57 GMT
WORKDIR /usr/share/kibana
# Wed, 24 Jun 2026 23:11:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 24 Jun 2026 23:11:57 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:11:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:11:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 24 Jun 2026 23:11:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:11:58 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 24 Jun 2026 23:11:59 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 24 Jun 2026 23:11:59 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 24 Jun 2026 23:11:59 GMT
LABEL org.label-schema.build-date=2026-06-18T10:33:37.467Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.6 org.opencontainers.image.created=2026-06-18T10:33:37.467Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=23c54dbd59f0a5bf5838a5ef65fadb4a6a4f1220 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.6
# Wed, 24 Jun 2026 23:11:59 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 24 Jun 2026 23:11:59 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:11:59 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 24 Jun 2026 23:11:59 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 24 Jun 2026 23:11:59 GMT
USER 1000
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e8fa8b7611c434071af131d093923c939e0aac590164854eb4bc1da660cc68`  
		Last Modified: Wed, 24 Jun 2026 23:13:05 GMT  
		Size: 19.3 MB (19289602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cc74b66c6482bf18bd9e41fe015325de6e92d7e2f87b397eaf8933f3dcf129`  
		Last Modified: Wed, 24 Jun 2026 23:13:13 GMT  
		Size: 400.8 MB (400833198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e04d5f7b4f261376aeae0929e3e28f22c13ddf0a83ce0b9d8bc204fe7601d`  
		Last Modified: Wed, 24 Jun 2026 23:13:04 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d35f74ea90d542f8bb836f650ce07241ada227b497cd9fd1f9fc06118143210`  
		Last Modified: Wed, 24 Jun 2026 23:13:05 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0d2ceb12614bc9d5d132042780120eb3a7c988054b965e26cbf0208ecb88de`  
		Last Modified: Wed, 24 Jun 2026 23:13:05 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d48c88d82d2e2bdb41e4505c68327823eabd39609f0bb30825273f59fc20a4`  
		Last Modified: Wed, 24 Jun 2026 23:13:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b832e5a5c1281075c0c6d6d3df56c2d9b59d483abc33c49732f90474fb54c4`  
		Last Modified: Wed, 24 Jun 2026 23:13:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40334c1e934ac40f8b13ed94ba76e9efe51db10d1902bac3f9dcaa7c10f2d12`  
		Last Modified: Wed, 24 Jun 2026 23:13:07 GMT  
		Size: 4.9 KB (4926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1633c3dcd065ddcc6f6a79a73cea521144501028be8af970e9dd87a20a769a`  
		Last Modified: Wed, 24 Jun 2026 23:13:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb3e5c52bf648de58ab5dc6c35be8db6807123281809f2d9812bd0f0a1f5225`  
		Last Modified: Wed, 24 Jun 2026 23:13:08 GMT  
		Size: 73.5 KB (73456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab838a81d9f12f934ae10b466ba30fc3da072d6be97da411baa03a3f51b1437a`  
		Last Modified: Wed, 24 Jun 2026 23:13:09 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed439dbb8581c8b9b427630c59994fd2e3c1e9d071f396fb9284c56faed89bc`  
		Last Modified: Wed, 24 Jun 2026 23:13:10 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.6` - unknown; unknown

```console
$ docker pull kibana@sha256:19fa7a6c5dd997d8250568b51a1ca254975cda4b173d43841e0ef74cb6bb8198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8fe2d08b657cd779288d7d7d5fc3339fd599d8e265318fa2e2729efa9b022b`

```dockerfile
```

-	Layers:
	-	`sha256:b02179b79f65d631aa0068ff4d4f1cbcf1bd0f04174b5d455b72d5cbf70c6da9`  
		Last Modified: Wed, 24 Jun 2026 23:13:05 GMT  
		Size: 5.8 MB (5811521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e324a832bb972116638bb1063eaeb1305063754c533f49492d722a83ca7d19b`  
		Last Modified: Wed, 24 Jun 2026 23:13:04 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.2`

```console
$ docker pull kibana@sha256:9e7a087494128d897d5446b15ac8766d16279e2dd238795bfe65faf4b68537ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.2` - linux; amd64

```console
$ docker pull kibana@sha256:5305e76951853e8c6555ca47f2e687522ba995e4973fcaa8e387697471f6da5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **535.3 MB (535306145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd12b18f6b795b78da83bdeac60b250f49e798ac8fae225472679cb042006f6`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:05:00 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 24 Jun 2026 23:05:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:15:00 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 24 Jun 2026 23:15:01 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:15:01 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 24 Jun 2026 23:15:01 GMT
RUN fc-cache -v # buildkit
# Wed, 24 Jun 2026 23:15:01 GMT
WORKDIR /usr/share/kibana
# Wed, 24 Jun 2026 23:15:01 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 24 Jun 2026 23:15:01 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:15:01 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:15:01 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 24 Jun 2026 23:15:01 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:15:02 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 24 Jun 2026 23:15:03 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 24 Jun 2026 23:15:03 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 24 Jun 2026 23:15:03 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Wed, 24 Jun 2026 23:15:03 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 24 Jun 2026 23:15:03 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:15:03 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 24 Jun 2026 23:15:03 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 24 Jun 2026 23:15:03 GMT
USER 1000
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bf8ddb11b5328780e23204d0f72ca49929efafdf22fa4f65183c1acdfe7647`  
		Last Modified: Wed, 24 Jun 2026 23:16:19 GMT  
		Size: 19.3 MB (19331101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4bc5eab6cafffd21becfe74edc071275de164186e024e6d0023db2f16e5bff`  
		Last Modified: Wed, 24 Jun 2026 23:16:28 GMT  
		Size: 458.7 MB (458745491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1007a7331c6d5df014e2b55a21982c4347e3b5c763a97a15c9ba5cb97ca355`  
		Last Modified: Wed, 24 Jun 2026 23:16:18 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae7dc7f909694cf50dad4d988b59795fd7a9469a0f81b8d7e3a422e00156eca`  
		Last Modified: Wed, 24 Jun 2026 23:16:19 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420b05da19ef6e42b91037f794fd9961a3cd4d89a7fa090163f1e39311601488`  
		Last Modified: Wed, 24 Jun 2026 23:16:19 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28275a98400dae8ba0809ad4cd42c2fed2897abaa9cdc6e3ce8f8e9f8e3e2d`  
		Last Modified: Wed, 24 Jun 2026 23:16:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25140cfdbf1af42bdf7820afa99c15cf0ff88a0e0ab20563ca8afa5942730f3e`  
		Last Modified: Wed, 24 Jun 2026 23:16:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec5b9a997f00d1fa1602b3b27ed988481e5a82fe51a238845bb2a8de67b615`  
		Last Modified: Wed, 24 Jun 2026 23:16:21 GMT  
		Size: 4.9 KB (4919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855f069137099c6bfdaee1f53d107ab465ae637309ef54f76b9806a77eaef3f0`  
		Last Modified: Wed, 24 Jun 2026 23:16:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c7c2c6d8056ac77eab160a0a8af2c2d39928031c0b2690a246870c8dc86f37`  
		Last Modified: Wed, 24 Jun 2026 23:16:22 GMT  
		Size: 74.5 KB (74545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d262f2e45eef98e0fcc20648c3e88d23f9f143700d38a6e045d189a077f94c8a`  
		Last Modified: Wed, 24 Jun 2026 23:16:22 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f70083e3e65a15a8bd94165503963b42f1de0df8c3c387826ac26921197f87`  
		Last Modified: Wed, 24 Jun 2026 23:16:23 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:e1ae73619966a29fe2776b7b6494bb1ac41af14833dc0a460b60c62886b2f478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6064341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa59f6e7164035dc775ce0186dfcc180177feff4c170cb30878dc8abe54705f`

```dockerfile
```

-	Layers:
	-	`sha256:89c3d5e819146638fc8cf0129b78577af7f4ff7a290b7b91514788fcd38e8805`  
		Last Modified: Wed, 24 Jun 2026 23:16:18 GMT  
		Size: 6.0 MB (6021115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567fb7a3f6b63ca6c9cdceee9edd9e4b8e58af33c0f42d01390d1636f0086341`  
		Last Modified: Wed, 24 Jun 2026 23:16:18 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f8ecd3f20f4762b3a55d9941583e4ab290731a7d5a566a9e0dfe4cc1058b9883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.3 MB (546269272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c286cc75730e5f6ebbb6d3baf8c2ec90063e2764529021ba79006b6a6f4a6c27`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:11 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 24 Jun 2026 23:04:11 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:12:16 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 24 Jun 2026 23:12:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 24 Jun 2026 23:12:17 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 24 Jun 2026 23:12:18 GMT
RUN fc-cache -v # buildkit
# Wed, 24 Jun 2026 23:12:18 GMT
WORKDIR /usr/share/kibana
# Wed, 24 Jun 2026 23:12:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 24 Jun 2026 23:12:18 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 24 Jun 2026 23:12:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:12:18 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 24 Jun 2026 23:12:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 23:12:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 24 Jun 2026 23:12:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 24 Jun 2026 23:12:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 24 Jun 2026 23:12:20 GMT
LABEL org.label-schema.build-date=2026-05-25T11:33:59.097Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=ca34dedcfe614964fe236c237a023021da0a8665 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-25T11:33:59.097Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=ca34dedcfe614964fe236c237a023021da0a8665 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2
# Wed, 24 Jun 2026 23:12:20 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 24 Jun 2026 23:12:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 24 Jun 2026 23:12:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 24 Jun 2026 23:12:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 24 Jun 2026 23:12:20 GMT
USER 1000
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc98605d400268a5cfe1da3478f8b97f83f0505e4775bf271e7ed29a5ef1be4`  
		Last Modified: Wed, 24 Jun 2026 23:13:41 GMT  
		Size: 19.3 MB (19289672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281df0374c1f55ed5c33291179a42de466bb84babaf1957e1122d8a06b85aca0`  
		Last Modified: Wed, 24 Jun 2026 23:13:50 GMT  
		Size: 471.6 MB (471616872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ef8940adf134f092ce954f3c25394b9b0202254b0955251ed826552fac3b62`  
		Last Modified: Wed, 24 Jun 2026 23:13:40 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f20a23a9e6110348ce7726e6a49cf8c1740ddcc6bdccf3622754697a84a597`  
		Last Modified: Wed, 24 Jun 2026 23:13:41 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787d4ce8db6b451638fe2e96019029eb4b4ff5e2e4fe9b3def61c714e310d03e`  
		Last Modified: Wed, 24 Jun 2026 23:13:41 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33532e7a662616a908c15a43fc3aff4f917c179bec724ea88294a7f4b2e6295`  
		Last Modified: Wed, 24 Jun 2026 23:13:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a789ccc0a9004b23124f415ba60a020cc6ff4eb7e4f32316fff0c1c2c55b6b`  
		Last Modified: Wed, 24 Jun 2026 23:13:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd33be5393b8b01abca67d08336715a727900de4596dacc9d84fcaac0dab4ed`  
		Last Modified: Wed, 24 Jun 2026 23:13:43 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf44cc6c38a02febb1800b7202b07aea4faa4319e5b7de31e71dd16bcebb4a`  
		Last Modified: Wed, 24 Jun 2026 23:13:44 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3bf7779f19f2abed56d962cbdb6456eae4ebf360c898e852aab69bbbd36bd0`  
		Last Modified: Wed, 24 Jun 2026 23:13:44 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be60b5c6f0cb1410a1d79cfe6c798ad77a7737e7c3f2cb728f9f76a9f779f195`  
		Last Modified: Wed, 24 Jun 2026 23:13:44 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c932c78453995cd27e880742bcb0a9bec2ad661237a6c1c21d167f9ae553e7`  
		Last Modified: Wed, 24 Jun 2026 23:13:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.2` - unknown; unknown

```console
$ docker pull kibana@sha256:80de73dc2f209df82e363f0ec7318e93bf40fe0d4d783baa362e66043c4321fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6063274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bf6fcb86f3e19118f3addf23700d0b80b060739a0a6e076a01240cdd08c45d`

```dockerfile
```

-	Layers:
	-	`sha256:e1751c0a005c3c1d91a2d29022f0fe76fd2de15452d3fa67c3e2d9cb984f92b6`  
		Last Modified: Wed, 24 Jun 2026 23:13:40 GMT  
		Size: 6.0 MB (6019791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17be8d3bd29d888cb5b572ba8b92123c6f66e4debf63486fe738b00b9e3ada5a`  
		Last Modified: Wed, 24 Jun 2026 23:13:40 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
