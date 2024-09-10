<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.1`](#kibana8151)

## `kibana:7.17.24`

```console
$ docker pull kibana@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kibana:8.15.1`

```console
$ docker pull kibana@sha256:826304508019ce346f35a6817b1e730c18efe2b5882bf12daec477060c98010e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.1` - linux; amd64

```console
$ docker pull kibana@sha256:426b9e373557bf62e6885aa98782505025d41f20100b069a310c75939d2926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393742062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0dde5a104ccd67354bd7538f97937b9942963e46d52dec64a90d8cf924284a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Sep 2024 16:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T12:15:21.436Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T12:15:21.436Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fdb71e81f1aab48fe4befba210ca076bee27c9ca7a9c74036983fe07eb77f5`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 10.9 MB (10945277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f38bcb526e838da90ffc8bdce23188725f29cabdc81b94a4dd49711ccfa18bf`  
		Last Modified: Thu, 05 Sep 2024 22:05:43 GMT  
		Size: 338.6 MB (338612904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb7acd1efc4f4ea7280b7bb2d31b715da2a447e03f9bb6b5a89fcd61030dfb1`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846f1629c72a6eb06ecccd8fdb1ec09e93b90a05b26bafbc4f29ca6727276c21`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce6b9672912b161e80b737151de4a4cc5edb1f61e51103e03737f8c00f393c5`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aab2c6e0fba6241730b041de8a36e1c1c535a5051e2dce9b016de3374a02b2`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f81ccb102c8fa5e7d5bcf38f08c1b25667c82b13952aa2cf520c387febbe2cb`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208be2ce3fe324c3b60ca9a08c42d48dbbb347b8176815fd750de341949530a8`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 4.6 KB (4627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8519ba4305d25228c6d62a46bf92f529f35e43c323b284aded34f190b0dff4e8`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53aaa438adccd4389f3be76872845d7319ab2dbc8935c53eba1c994cb1ab66`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 189.4 KB (189430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c108aac256f036478ad3e192075be59e27990d0fdc8ca93803bcfc10b6090681`  
		Last Modified: Thu, 05 Sep 2024 22:05:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.1` - unknown; unknown

```console
$ docker pull kibana@sha256:8cf439d59109dbab0a84c1b2eb1429a3a689fa731e26953a5f6a711bb8182cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4103967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb8dd79606ee06e81ead98b0723dd86a4bdb203c5c3d1b9908a2997fd7ff254`

```dockerfile
```

-	Layers:
	-	`sha256:2220ecce9ce8bd7409c827767dd36c3c279905ac8d4f4af20449dfb5f160d03f`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 4.1 MB (4063579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef92ee7d97b53f99ff9d9a72abeadbe370c71dfab34187f6457adfa4b8f83b42`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 40.4 KB (40388 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0723e618fbb73c4e4fb85dd8db1b94031aaf96d39954e6e66d7a7ce82b32f74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404648844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec167ad0e8d996730439ac291a9114b03863932e5908f69735fb0bf73faf7def`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Sep 2024 16:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T12:15:21.436Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T12:15:21.436Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdedf750a744afb7e0b04b26877aee1247d6f9ea65ba56552f24a1e9924a4a8f`  
		Last Modified: Sat, 17 Aug 2024 02:58:25 GMT  
		Size: 10.8 MB (10797079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67bbe7b6b7cf2f5aa1b7074695ee58bdfbb78703ae71443d4a2399b2772950`  
		Last Modified: Thu, 05 Sep 2024 22:19:44 GMT  
		Size: 351.2 MB (351211846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad594e431daa16b323ee60eaa4a41bb2712e36d6abb364a2241d98d9f3d6ccb`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a6c171b38d01f72d4ea8f5248aca5bfc24c14358e647a9919026bd3e04021`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca544c9570d1048f3e9bbd6be835c61deb7bc868a4e6906859644370737c530b`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 5.3 KB (5298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd8aae931d61ddfff3a278853ab881df32709bdf8dc383cbe3959e5eb1d1da4`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61633fd72db7111f7b16095a54e20aaf28c97ec71bc98706055df82c800771`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603599a53019ffbb9514220fdf858648d0c35bf7a55db356819c3f0d590d5c92`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6ba2a0bb454ff9eef46c7bd1c4f9b6ae0acd28cdb12ed6983c6de8177248a`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08571e2eb63d047e75cd36fd4f48645ff2899d5c6da2df30093e30e748a9d76`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f24bc4a7595e6c6fe9e52b3f6d21d7efd3126096fe17475da1a23c631c6cb`  
		Last Modified: Thu, 05 Sep 2024 22:19:39 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.1` - unknown; unknown

```console
$ docker pull kibana@sha256:fccf0bf0652985000c9ada30b61f1ec3e0de4327c272e9e38943aeaea0a9f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4104481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c261549449f8b65a1e1338bb85124133f418caa2728ccc4d3870a73107f67483`

```dockerfile
```

-	Layers:
	-	`sha256:cd2717e09601bc29b2b62d5caf5bb9cc2cbc39df3d3060788924df14f0c7a859`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 4.1 MB (4063829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cecb08a450809924cae3019c818a66407f573cf16955ac96992a8093f2f03a6`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 40.7 KB (40652 bytes)  
		MIME: application/vnd.in-toto+json
