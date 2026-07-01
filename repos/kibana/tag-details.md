<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.18`](#kibana81918)
-	[`kibana:9.3.7`](#kibana937)
-	[`kibana:9.4.3`](#kibana943)

## `kibana:8.19.18`

```console
$ docker pull kibana@sha256:99dd7d8e0165a50dccbbb4830a025d3df1a231c9c6b3835312a5b9c496bb20ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.18` - linux; amd64

```console
$ docker pull kibana@sha256:f64e9447dc0816b9c769ae36e6d4a8d181d3857bf95b7cde0ce8566113ae8e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **457.2 MB (457171075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1311482cc1635f7779b22551b8a309d7a818d561aba9b965939d28878a269b`
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
# Tue, 30 Jun 2026 23:25:41 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 23:25:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:40 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 23:33:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 23:33:40 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 23:33:41 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 23:33:41 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 23:33:41 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 23:33:41 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:33:41 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:33:41 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 23:33:41 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:33:41 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 23:33:42 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 23:33:42 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 23:33:42 GMT
LABEL org.label-schema.build-date=2026-06-26T06:55:50.831Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8b2d519956d8e256d1da1a46185994fee710c3b8 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.18 org.opencontainers.image.created=2026-06-26T06:55:50.831Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8b2d519956d8e256d1da1a46185994fee710c3b8 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.18
# Tue, 30 Jun 2026 23:33:42 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 23:33:42 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 23:33:42 GMT
USER 1000
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4febed2992e7ac11c15746e4b3230253374807e86047e979fce2655a1b2618c`  
		Last Modified: Tue, 30 Jun 2026 23:34:43 GMT  
		Size: 11.8 MB (11800039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b535ea48731a162d9f6b7afc8cafc36badaec52ca0420c3cc12f049d643789`  
		Last Modified: Tue, 30 Jun 2026 23:34:51 GMT  
		Size: 399.0 MB (398994222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3430f55661e426d7c1d6214163bf2aaaf5e3bedf3ba3c62214682dc76737b69f`  
		Last Modified: Tue, 30 Jun 2026 23:34:42 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5682c0231b74baa47a1bb076bccbbfbef543343fb37fa8e71a209f7962e3b81a`  
		Last Modified: Tue, 30 Jun 2026 23:34:44 GMT  
		Size: 16.5 MB (16460474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d471b850cf5eb4319bc5f1f3d984c05f3adca7ae9dfee8bc3589ca18537d80`  
		Last Modified: Tue, 30 Jun 2026 23:34:44 GMT  
		Size: 5.2 KB (5248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3344ed65426fc72b9afcc56a884e5a62e810bb2d486fcde7d3eb7933c70be9`  
		Last Modified: Tue, 30 Jun 2026 23:34:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179624183ebb283ca8dae639aa0375010357afd889b54968753bbed04ba52662`  
		Last Modified: Tue, 30 Jun 2026 23:34:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cce18f84afeab5152062b03ea551773c8f30b173ec571f6368651b9842ead7`  
		Last Modified: Tue, 30 Jun 2026 23:34:45 GMT  
		Size: 4.8 KB (4823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7514656c19d3d0d8cabe6a9724c0cb95d51b0af4aab85c8ac9fdcb392bbf8d7`  
		Last Modified: Tue, 30 Jun 2026 23:34:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6432b59533a425f4d807290d8bb78ed7d944c5b32ca1c1c2717eece67dd43c`  
		Last Modified: Tue, 30 Jun 2026 23:34:46 GMT  
		Size: 161.7 KB (161744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625df51eff799d879810782899f30d9bfa68ff7e110975048821a73426eaa02d`  
		Last Modified: Tue, 30 Jun 2026 23:34:46 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.18` - unknown; unknown

```console
$ docker pull kibana@sha256:aaec4729c1ce1c5fb27d54514882dffadc633ab3721af1b0fe417ee2f5df57e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4964544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30478161c64a3705b4280e22f4c843bc2297fcdeff194ef31003540d865cf69a`

```dockerfile
```

-	Layers:
	-	`sha256:9b6d6a22b9ac1762da1838da883cd966075c18e25cf1f722f453b905e9ee100c`  
		Last Modified: Tue, 30 Jun 2026 23:34:43 GMT  
		Size: 4.9 MB (4923617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dad67fb0c4f044b329a57799d05b39b1472993d4d29e0c563767f877a78ebf`  
		Last Modified: Tue, 30 Jun 2026 23:34:42 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.18` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1ed178704213e14f5ceff303d99545ed8c503a786fbdcaaeb8c773cf5106ee65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.0 MB (468989200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53db2c7e986d7c8251c98aefbe9182d84383071f1ee36aada4b0840f388bf88`
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
# Tue, 30 Jun 2026 23:25:10 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 23:25:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:31:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 23:31:58 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 23:31:58 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 23:31:58 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 23:31:58 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 23:31:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 23:31:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:31:58 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:31:58 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 23:31:58 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:31:59 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 23:32:00 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 23:32:00 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 23:32:00 GMT
LABEL org.label-schema.build-date=2026-06-26T06:55:50.831Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8b2d519956d8e256d1da1a46185994fee710c3b8 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.18 org.opencontainers.image.created=2026-06-26T06:55:50.831Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8b2d519956d8e256d1da1a46185994fee710c3b8 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.18
# Tue, 30 Jun 2026 23:32:00 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 23:32:00 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 23:32:00 GMT
USER 1000
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e730977a0b770b9efb57f513249a3d055ada44aa5f0db30f042c827efcaca48`  
		Last Modified: Tue, 30 Jun 2026 23:33:08 GMT  
		Size: 11.6 MB (11633098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784aa628d56482c2b1941ec7dcba70913054ab867bb695bb2bc35d2f4b694937`  
		Last Modified: Tue, 30 Jun 2026 23:33:16 GMT  
		Size: 411.8 MB (411839600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6038c86c10c2d3d7cd6e2b14b4f7c43e926aedfb72bc8305d8117a678931dba`  
		Last Modified: Tue, 30 Jun 2026 23:33:07 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df31039c001cbf56c6b3e6283755786c7762b575ebf41866d2a6faabc1cb1a39`  
		Last Modified: Tue, 30 Jun 2026 23:33:08 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c458cdc66b823c4744fb073fd8b28f42f5df69641f7a15259c7dc52d2d9a26ba`  
		Last Modified: Tue, 30 Jun 2026 23:33:08 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78781b66695fe6c28aee3f51513ed926b3b821e613fdf25ec4c29080c88a84a8`  
		Last Modified: Tue, 30 Jun 2026 23:33:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4915a4fda0eca4eb81f8965355151d3b8c1139ab0992f171b572c1d9f6a8cf37`  
		Last Modified: Tue, 30 Jun 2026 23:33:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e87a0729760ff1623c72064b5062003897459f3b21ab6be4dcdbd71580f685b`  
		Last Modified: Tue, 30 Jun 2026 23:33:10 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a022bc0b7b3484c2960166178d713ff87c11bfd1e18519e8cd0776d9552b68`  
		Last Modified: Tue, 30 Jun 2026 23:33:11 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e1de1ebb3e585ec15b292a268bb77d41e82109611087edf359deef73389bbb`  
		Last Modified: Tue, 30 Jun 2026 23:33:11 GMT  
		Size: 158.3 KB (158261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc7d1dc74605502a886a5538f79ecdb6fcb4b04059e0b9919a8a8920e11a8e0`  
		Last Modified: Tue, 30 Jun 2026 23:33:11 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.18` - unknown; unknown

```console
$ docker pull kibana@sha256:6f8e319031857e30f1470446de795938d2cbddb256c7fa2f60d1d1f1bd685afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a316a70c6483bed1238adedc76eccb9adc63e14ee172552680f0b4fd0858a36`

```dockerfile
```

-	Layers:
	-	`sha256:c3f2f38d47e4e3dea07020c3aa5ee156167000351df85f5d275c2ef2f83f7167`  
		Last Modified: Tue, 30 Jun 2026 23:33:07 GMT  
		Size: 4.9 MB (4924681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a858b2e8639ee825e976d4df206f0763e12f5accae4d71534444fab7a7123a8`  
		Last Modified: Tue, 30 Jun 2026 23:33:07 GMT  
		Size: 41.2 KB (41175 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.7`

```console
$ docker pull kibana@sha256:da40c7b54de1fb4dc924ae143f1c04afa53ab2b70eddb3c62fd242ecf846c65a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.7` - linux; amd64

```console
$ docker pull kibana@sha256:fbe979c15f8450c3c4653be5bc44909f670143b4744cf126cdc1e74521b3c581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.2 MB (466170934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde738e76e4a778f852d0638f4f018457df7eabd2340d2804919826b3da49272`
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
# Tue, 30 Jun 2026 23:25:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 23:25:47 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:33:37 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 23:33:37 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 23:33:37 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 23:33:38 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 23:33:38 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 23:33:38 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 23:33:38 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:33:38 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:33:38 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 23:33:38 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:33:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 23:33:39 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 23:33:39 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 23:33:39 GMT
LABEL org.label-schema.build-date=2026-06-25T18:50:47.749Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=36e00282a99d328a291ef2eefb94fe83b741dd19 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.7 org.opencontainers.image.created=2026-06-25T18:50:47.749Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=36e00282a99d328a291ef2eefb94fe83b741dd19 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.7
# Tue, 30 Jun 2026 23:33:39 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 23:33:39 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 23:33:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 23:33:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 23:33:39 GMT
USER 1000
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb273e693c866f7bfc29ca7c18da9d8948dd6c2808ca4a549839af01f26dfb26`  
		Last Modified: Tue, 30 Jun 2026 23:34:38 GMT  
		Size: 19.3 MB (19331511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d527500eb67b71d48d6d7cb4f5c2a1dd68e0a0a2512076fec5eca5482e3c43`  
		Last Modified: Tue, 30 Jun 2026 23:34:45 GMT  
		Size: 389.6 MB (389594177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff944f57b54976f49f82403dcff35db7cde5f542eacd0b814c379759244230b`  
		Last Modified: Tue, 30 Jun 2026 23:34:36 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d584012063c6133146afc13395dec5fb0ded6834c91bcd7e47c5fe6545b3422`  
		Last Modified: Tue, 30 Jun 2026 23:34:38 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dad7833e956946283fdfa28020df6e346ea41ce48b927ddbce86c19474e108`  
		Last Modified: Tue, 30 Jun 2026 23:34:38 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b7c469e3fe1a6771e607944df9d9cf580e04e726bb3babc451b06fdb49c22a`  
		Last Modified: Tue, 30 Jun 2026 23:34:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49058a54ee01b0056fa22324d46f1bd4ed1f0cc92ab45554987d11bcc40648c2`  
		Last Modified: Tue, 30 Jun 2026 23:34:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfd4963720db578222513fb71b2c0196aa21f2093e5727e6a10038ca8675651`  
		Last Modified: Tue, 30 Jun 2026 23:34:39 GMT  
		Size: 4.9 KB (4929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6af5926150f5fbe9531b37612a5ece2e12e88fcaa58a7deb1b63634238009d`  
		Last Modified: Tue, 30 Jun 2026 23:34:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138ca0133bae6a09fb355f4bdfb7f0781c7ee026792979e47dcfcd7d4a599f6c`  
		Last Modified: Tue, 30 Jun 2026 23:34:40 GMT  
		Size: 74.5 KB (74547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c35ebeceab066655f5d8ece5b24635f1da0c4c38f0b12223ddd9a1ec346f33`  
		Last Modified: Tue, 30 Jun 2026 23:34:41 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e7fe0f31851e0faf552745ee1cbf69fa583677f9c05a7bc5c3f51e1839319c`  
		Last Modified: Tue, 30 Jun 2026 23:34:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.7` - unknown; unknown

```console
$ docker pull kibana@sha256:b0a63c715f031108957ae400351c20007d4c7ab6dae8c925f100e8638253cb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5817011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22652819a4314dafb584c8ecdfb7a53a0d913953ccdfa97962dbe18dd2b1395a`

```dockerfile
```

-	Layers:
	-	`sha256:57c0566e4f46afd96428c4e31bcbca0aed299be4d60f79b7f7f2a323fb3826e9`  
		Last Modified: Tue, 30 Jun 2026 23:34:37 GMT  
		Size: 5.8 MB (5773785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23fd9c19b22a0715d383c884f3d535f052aac5de9563301f1f6cf35ce34290a6`  
		Last Modified: Tue, 30 Jun 2026 23:34:36 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d4013549076e00700b3ba6b6aca1866d9ad7d77d4f7b2d55be8f4ccde8443bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.1 MB (477122447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cff5560f79529a6cc7c9096455ee5ec404c2d2556c6180fe97238f3ada4d98`
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
# Tue, 30 Jun 2026 23:25:38 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 23:25:38 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:32:06 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 23:32:06 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 23:32:06 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 23:32:07 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 23:32:07 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 23:32:07 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 23:32:07 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:32:07 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:32:07 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 23:32:07 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:32:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 23:32:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 23:32:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 23:32:09 GMT
LABEL org.label-schema.build-date=2026-06-25T18:50:47.749Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=36e00282a99d328a291ef2eefb94fe83b741dd19 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.7 org.opencontainers.image.created=2026-06-25T18:50:47.749Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=36e00282a99d328a291ef2eefb94fe83b741dd19 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.7
# Tue, 30 Jun 2026 23:32:09 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 23:32:09 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 23:32:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 23:32:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 23:32:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be9b01ff906b3735a89d9f39c85dfe2b6f036671a631542d07e7a49d21da0e`  
		Last Modified: Tue, 30 Jun 2026 23:33:15 GMT  
		Size: 19.3 MB (19283498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097ac118e4033497849508b39213b4f22fdde6fe564fbe3b7d07caa4906229ed`  
		Last Modified: Tue, 30 Jun 2026 23:33:23 GMT  
		Size: 402.5 MB (402462597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2dfcc08fe99078c4e848293c72d5051decf6610d438f8adf85f5511840a705`  
		Last Modified: Tue, 30 Jun 2026 23:33:14 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff71eb64374fc4a75dc213db13da71a95445ce783110c8a0f456742e0dd21a8`  
		Last Modified: Tue, 30 Jun 2026 23:33:15 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc4663d859dc3b382a70584235c9fbafebd56c9f9d5689624548ab1313e480b`  
		Last Modified: Tue, 30 Jun 2026 23:33:15 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7ff471a79f7c446a29f451cdd3de6b253967b2fecbfbbca189e572e0da70fa`  
		Last Modified: Tue, 30 Jun 2026 23:33:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a90026347a46e921d0d650e991f6809685f345fe2a1ef3f8722438d649130`  
		Last Modified: Tue, 30 Jun 2026 23:33:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2283541f9c1a6faf9bd7cb6c3cd8017f9c7c25e5e9155fc2f85372a199c32c`  
		Last Modified: Tue, 30 Jun 2026 23:33:17 GMT  
		Size: 4.9 KB (4924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a9cef030c161a639e535cd4a2d3332ca459fe7953e707714393a59567c3599`  
		Last Modified: Tue, 30 Jun 2026 23:33:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1b96d42dcc6c7eadab1d3c67f5f567b6a6bcc43bfa8e8bef566c31f782aa`  
		Last Modified: Tue, 30 Jun 2026 23:33:18 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0402fd3c176c7d0216bf7e99a1e8499e62cbeac644f8ac7f791ce050975f31d1`  
		Last Modified: Tue, 30 Jun 2026 23:33:18 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5eee160dc6d1bdf15525c52b15162b68a2969025e83106d08ba182df58b005`  
		Last Modified: Tue, 30 Jun 2026 23:33:19 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.7` - unknown; unknown

```console
$ docker pull kibana@sha256:f3b508e274e000af3f3c5361898e2c4eec65e37d47716fe1db6b386726f3bee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5814158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b0e337bee644ab1eb3190c717dd6924a4e0d6989fad9f692fabdc09d253284`

```dockerfile
```

-	Layers:
	-	`sha256:9db558d611d7eef2bc54dc6bff82b778c729a16b03eab18a89769b9f6445e5f3`  
		Last Modified: Tue, 30 Jun 2026 23:33:14 GMT  
		Size: 5.8 MB (5770675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921730dd5d0433b0089f99842c733fe81e5a26f6eead3aadaed9414775419e21`  
		Last Modified: Tue, 30 Jun 2026 23:33:14 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.4.3`

```console
$ docker pull kibana@sha256:b81e350e6444f4e1a79384354f8c6f6d07e099d0059db0c78096f896855217b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.4.3` - linux; amd64

```console
$ docker pull kibana@sha256:14a9dc312034d4f5e4a57cfdf910e291d8e0a1fe54837ca60dc991cc266f0f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.5 MB (531519283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dc44665659df1d0be111cf1fe6f092b58f08c01ecf459c13d7f03611da6e96`
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
# Tue, 30 Jun 2026 23:26:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 23:26:14 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:35:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 23:35:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 23:35:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 23:35:13 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 23:35:13 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 23:35:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 23:35:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:35:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:35:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 23:35:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:35:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 23:35:15 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 23:35:15 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 23:35:15 GMT
LABEL org.label-schema.build-date=2026-06-25T16:11:43.052Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9e9848d35f973e1f40f65d79760037228c54b7ab org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.3 org.opencontainers.image.created=2026-06-25T16:11:43.052Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9e9848d35f973e1f40f65d79760037228c54b7ab org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.3
# Tue, 30 Jun 2026 23:35:15 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 23:35:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 23:35:15 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 23:35:15 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 23:35:15 GMT
USER 1000
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd4deff32fe92b5675987cd8fddb32c0bed1e962bd9f29d2d812a77bae298`  
		Last Modified: Tue, 30 Jun 2026 23:36:20 GMT  
		Size: 19.3 MB (19331437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e18cc1a827ac4d4fa1b2e2a08aa867e0ff65896791aa2e83eadb3fdaaa8850c`  
		Last Modified: Tue, 30 Jun 2026 23:36:29 GMT  
		Size: 454.9 MB (454942595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729cc8273abce952050d3d2b2480e672145389b6f014d73e21118a8a3a149c9`  
		Last Modified: Tue, 30 Jun 2026 23:36:19 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b78c426181529140963b73961988dc00d482576e305a24731f14cccc2954981`  
		Last Modified: Tue, 30 Jun 2026 23:36:20 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b97c6c1b30c246a1075c2f9fcf9b1ab8d7b63c218f9c7432716e812874ae360`  
		Last Modified: Tue, 30 Jun 2026 23:36:20 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69877d6b338259d91a1882ff609573c4396ddbf660ddd1a136c4ca86cd6128e`  
		Last Modified: Tue, 30 Jun 2026 23:36:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92b86e88b9649ac41f136da6179fb5aff11d88f4ae3fca4db68f137f208795f`  
		Last Modified: Tue, 30 Jun 2026 23:36:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a013021de1949869731765f7da1e1898a06307a5f8020be332dc53e3b76e0faa`  
		Last Modified: Tue, 30 Jun 2026 23:36:22 GMT  
		Size: 4.9 KB (4928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8215745b520b95c0d6f099ca909935f32abef26f4e42ed524aee498ff9ab12`  
		Last Modified: Tue, 30 Jun 2026 23:36:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4195d4d51a3fcd87f25e2ff1619267d80c9824027aedd411ec8b9f9e630f0f0`  
		Last Modified: Tue, 30 Jun 2026 23:36:23 GMT  
		Size: 74.5 KB (74548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7722a1a5ca12ea8204919ea68dceed533267c10d4d853ba2a127efd3ac2c0d`  
		Last Modified: Tue, 30 Jun 2026 23:36:23 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227eeda62df119cf20b5ae6e37f66875ca7f9c8ea26e116faa28a4f0f9a8fc8`  
		Last Modified: Tue, 30 Jun 2026 23:36:24 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.3` - unknown; unknown

```console
$ docker pull kibana@sha256:5f72308be6ca0906d202c27e0e55330c669ec54883a83a7107df02f706bda9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5885649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ad973df83775ec58e508ce99ff075f07fa7c946cc546869ade22a9a5b61a3a`

```dockerfile
```

-	Layers:
	-	`sha256:ea2eb92407156f82e51fc4f44c68767b12fd47912dd4d20c9b2ebc407a2ee8ac`  
		Last Modified: Tue, 30 Jun 2026 23:36:19 GMT  
		Size: 5.8 MB (5842423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5567ce243838af0923abf6a64baae9ec42da8dbf41a5381c682b4c2a3d859e8a`  
		Last Modified: Tue, 30 Jun 2026 23:36:19 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.4.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6e8b89ce039499ce0948fce35edd9d83a99f504faaa0433bb28c061df4893de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542564657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d1026ca79b9733f0017cb49fe6a491fefd0762bbf1824667c91fa77785d665`
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
# Tue, 30 Jun 2026 23:25:46 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jun 2026 23:25:46 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 30 Jun 2026 23:32:42 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jun 2026 23:32:43 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jun 2026 23:32:43 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jun 2026 23:32:43 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jun 2026 23:32:43 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jun 2026 23:32:43 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jun 2026 23:32:43 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jun 2026 23:32:43 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 23:32:43 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jun 2026 23:32:43 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 23:32:44 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jun 2026 23:32:45 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jun 2026 23:32:45 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jun 2026 23:32:45 GMT
LABEL org.label-schema.build-date=2026-06-25T16:11:43.052Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9e9848d35f973e1f40f65d79760037228c54b7ab org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.4.3 org.opencontainers.image.created=2026-06-25T16:11:43.052Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9e9848d35f973e1f40f65d79760037228c54b7ab org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.3
# Tue, 30 Jun 2026 23:32:45 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.4.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 30 Jun 2026 23:32:45 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 30 Jun 2026 23:32:45 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jun 2026 23:32:45 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jun 2026 23:32:45 GMT
USER 1000
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0443f50a73bf282ef2b70a6da0467ec1375b3c1cadd87fdfede776b6b4fdb891`  
		Last Modified: Tue, 30 Jun 2026 23:34:04 GMT  
		Size: 19.3 MB (19283469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd46cbf7676e57113133519602504e31e9e0e94be5bc08e495a86e4a28980e9f`  
		Last Modified: Tue, 30 Jun 2026 23:34:13 GMT  
		Size: 467.9 MB (467904833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2539279219f802fc590105f7dea6fc7eb97daa99a9bd433cc4a2bb3a2950bdf4`  
		Last Modified: Tue, 30 Jun 2026 23:34:03 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07bfe43b2a6e9160411e4e0d472365e81f93ebe31da8787b80f73053baca20`  
		Last Modified: Tue, 30 Jun 2026 23:34:04 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395fc4a0e46e844d33060c2fcec8ce0b8cb155c8609628e4131ce36c4119d81d`  
		Last Modified: Tue, 30 Jun 2026 23:34:04 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f41afcbc7dbaaa972821093131f231a9491069beaba88db8afc94ff38556e7`  
		Last Modified: Tue, 30 Jun 2026 23:34:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:becfff45c48a707e54feabca8b062dff8b5ed30dc725c4bd629f6a63fd2f9c6f`  
		Last Modified: Tue, 30 Jun 2026 23:34:06 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b99875ca9b41bdec829b76545a04f47feb6a98b7fc4cddc539bc1fd1524eb9`  
		Last Modified: Tue, 30 Jun 2026 23:34:06 GMT  
		Size: 4.9 KB (4928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e273b7e87454a122c7d3c454e138a7cb2662523e77f9c02fe38744ec80b66f`  
		Last Modified: Tue, 30 Jun 2026 23:34:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03ab54d35b4a4d9d23c4fcca549d275e785c498a388487902f35185f5a9ab9f`  
		Last Modified: Tue, 30 Jun 2026 23:34:07 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1af7c3b27710a9d944251c126ee39058ffdb9f29af9c0cb79ba12a23f97f6f3`  
		Last Modified: Tue, 30 Jun 2026 23:34:07 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2c326ee0317a40adaa9995c8991bb299edeeaecd20d36ac52d69ffffd427f5`  
		Last Modified: Tue, 30 Jun 2026 23:34:08 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.4.3` - unknown; unknown

```console
$ docker pull kibana@sha256:45a4a4e7b10a5b79e47f91c9895f80166fab8ff67514cdd7f3e13cd436f07c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5882796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b36fe0f9719fef130d477bbd6dba7ccae6e95abdaea8a70a9b4c90654768d22`

```dockerfile
```

-	Layers:
	-	`sha256:cbbd67b69b38afdfad6063659f5a983da6fc13789b5be100effb44cb578b7bfa`  
		Last Modified: Tue, 30 Jun 2026 23:34:03 GMT  
		Size: 5.8 MB (5839313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7dfd8c284ae9e5611ec4ee5263bde80c097c2c5845b305e345f63a19fc632c`  
		Last Modified: Tue, 30 Jun 2026 23:34:03 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
