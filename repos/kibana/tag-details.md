<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.16`](#kibana81916)
-	[`kibana:9.3.5`](#kibana935)
-	[`kibana:9.4.2`](#kibana942)

## `kibana:8.19.16`

```console
$ docker pull kibana@sha256:9ec9531a9770493fd0649d18922aab5b25431dbaa7b7634caf9c609a1e2a745d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.16` - linux; amd64

```console
$ docker pull kibana@sha256:4cbb55598eb9a7d6b02acd5efc923cff86ca51e02c3ed5c07306acb8892fdec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.6 MB (455578035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c8c4a41f4f816b70ca706e94f31f81cdd3e3d48a14eed4451d5a4654d12db1`
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
# Thu, 28 May 2026 21:34:16 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 May 2026 21:34:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:43:01 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 May 2026 21:43:02 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:43:02 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 May 2026 21:43:02 GMT
RUN fc-cache -v # buildkit
# Thu, 28 May 2026 21:43:02 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2026 21:43:02 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 May 2026 21:43:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:43:02 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:43:02 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 May 2026 21:43:02 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:43:03 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 May 2026 21:43:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 May 2026 21:43:04 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 May 2026 21:43:04 GMT
LABEL org.label-schema.build-date=2026-05-25T11:13:36.011Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T11:13:36.011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Thu, 28 May 2026 21:43:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 May 2026 21:43:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 May 2026 21:43:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9711b0f4184869fecf4f0d8c21738a8fd45e31411cf6b61a8b4d8038827d57e0`  
		Last Modified: Thu, 28 May 2026 21:44:07 GMT  
		Size: 9.4 MB (9435895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6abfc26a5d353beba2222c5c101ca98024179a40f948d1d86795d2b0907d76`  
		Last Modified: Thu, 28 May 2026 21:44:15 GMT  
		Size: 399.8 MB (399765149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59619f70c4e85687ff4c3ce8969bc9fc9c9cd4d026115867cf8f989973eda2d`  
		Last Modified: Thu, 28 May 2026 21:44:07 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6d8314d3bb60cfd4e5b900fd2820ae740be70012917f8c05ccccc6dfb11a7`  
		Last Modified: Thu, 28 May 2026 21:44:08 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ed53694e03aeee4f4387883d57d1de23e5b96798c5b5d4148e08e536f1cc6d`  
		Last Modified: Thu, 28 May 2026 21:44:08 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cc9bc90acab4d0f02769c939bce0ea37143b803cb69e68b55d213334561ddf`  
		Last Modified: Thu, 28 May 2026 21:44:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f375e778dbd317cc28088b82b6b49e3301b0d207dc5b28c894aa42fd11a3d925`  
		Last Modified: Thu, 28 May 2026 21:44:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ada91f025ce1e52f4fb35528ef14100b6b63214177881ea2a9043b17f917828`  
		Last Modified: Thu, 28 May 2026 21:44:09 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3a90094205cccccb4f6ced059ce9b65be61522bec12f16e301629120d48bbd`  
		Last Modified: Thu, 28 May 2026 21:44:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f79556b7671c4ebeafc1f2f0ef861ff07e39b85badced30220b08975bc335`  
		Last Modified: Thu, 28 May 2026 21:44:11 GMT  
		Size: 161.7 KB (161743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b4b7c10b05b7a0bae29328e2e07e7e02923387506ba12869151b95b4253e3b`  
		Last Modified: Thu, 28 May 2026 21:44:11 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.16` - unknown; unknown

```console
$ docker pull kibana@sha256:b457627fd25dade919b7892134e29cbf6a5717286955a5ce891545f0598073fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26710563374a3e6d44b7ea5e8a66858a7feab1434ff3dc02624c2f026720f7b5`

```dockerfile
```

-	Layers:
	-	`sha256:aef17f48af1c55c3634eff38182e8e781a6fb3f5e17dde47354c91246c6658ce`  
		Last Modified: Thu, 28 May 2026 21:44:07 GMT  
		Size: 5.0 MB (5029663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b9019c4be4853d9cdc99a2e77b6a56f2706319acc5388f11303e41393ed23d9`  
		Last Modified: Thu, 28 May 2026 21:44:07 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.16` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1f9d97cebf3248547c83a678de4b7656236c93f066b00f154782118970f02af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467503990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dcf0cc1a9f5a115d820e9a6ed4daa3b0f2b58e836f60a2299c504a10388bea`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:34:22 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 May 2026 21:34:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:41:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 May 2026 21:41:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 May 2026 21:41:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 May 2026 21:41:13 GMT
RUN fc-cache -v # buildkit
# Thu, 28 May 2026 21:41:13 GMT
WORKDIR /usr/share/kibana
# Thu, 28 May 2026 21:41:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 May 2026 21:41:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:41:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:41:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 May 2026 21:41:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:41:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 May 2026 21:41:15 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 May 2026 21:41:15 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 May 2026 21:41:15 GMT
LABEL org.label-schema.build-date=2026-05-25T11:13:36.011Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.16 org.opencontainers.image.created=2026-05-25T11:13:36.011Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=209c12d77d1bf1bc561abff2b91aa95f354734a3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.16
# Thu, 28 May 2026 21:41:15 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 May 2026 21:41:15 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 May 2026 21:41:15 GMT
USER 1000
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f33ddc78303e36b2d2e400a5ea33aa7d14292ed8f6a8886f75927b403f9e43`  
		Last Modified: Thu, 28 May 2026 21:42:24 GMT  
		Size: 9.5 MB (9455656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e9c842e17a286fd7e7c34e357eef4fae4aa8ea07d5a3e81a0f2c511073b9c`  
		Last Modified: Thu, 28 May 2026 21:42:34 GMT  
		Size: 412.5 MB (412532453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a2c202be77ff0642a496cdddca875b8e7b45750eab2a7f6e1de79e09758111`  
		Last Modified: Thu, 28 May 2026 21:42:24 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac17c6bd537fd2858ec88e927f468edde7184398bd6823039e90b80bc947cbbe`  
		Last Modified: Thu, 28 May 2026 21:42:25 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200908fdc967cad3a4c375faa923bf882c9c1613201b4d44a267c1b704161beb`  
		Last Modified: Thu, 28 May 2026 21:42:25 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35040df483325ed8a5fc961a7cdee8ebcf8dafc8cc88b89035dca87a49f12765`  
		Last Modified: Thu, 28 May 2026 21:42:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3688d0dbc6c954ad37dace0da66b8ecd3876171c938091c92121bfd6e9b3c7e8`  
		Last Modified: Thu, 28 May 2026 21:42:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2827143e9781bdf0eaa991e0bf4d014fa228fe4238d0c9b734302e56db8551`  
		Last Modified: Thu, 28 May 2026 21:42:26 GMT  
		Size: 4.8 KB (4819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa601d69dd3e93a84fade512aed05d64b5e2ff3fd903a4c1c97491aad07b83b6`  
		Last Modified: Thu, 28 May 2026 21:42:28 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47985356b513a82c01211a9e7171e022d1fa1eff4dbd758b4fe5ab65848ffa21`  
		Last Modified: Thu, 28 May 2026 21:42:28 GMT  
		Size: 158.3 KB (158262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554a8ad64ecf4c2c824499d5df5047bd9cd8cb9aaa0954942907e1d7ab4af8a1`  
		Last Modified: Thu, 28 May 2026 21:42:28 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.16` - unknown; unknown

```console
$ docker pull kibana@sha256:4beafe87a31c6c4b5273e23df98ac41f699617348419416efbee1627d0177e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f412021f132cac32d221c5be271a10ff9f5b2df98c4addcdb7be156589b6bcc`

```dockerfile
```

-	Layers:
	-	`sha256:445daaecb50545d79a4f49d32a0a5c627d6b6cace6eb50ad6c62382e8f7514b2`  
		Last Modified: Thu, 28 May 2026 21:42:24 GMT  
		Size: 5.0 MB (5030727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f0523e7b803679092d3a4a10144e6c033d075173db2cbc2110ff19976d85b8`  
		Last Modified: Thu, 28 May 2026 21:42:24 GMT  
		Size: 41.2 KB (41163 bytes)  
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
