<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.16.4`](#kibana8164)
-	[`kibana:8.17.2`](#kibana8172)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kibana:8.16.4`

```console
$ docker pull kibana@sha256:9b32aa01806b6f35146daf1baa8c0f3b2e5e2d818b5128dd8e4d0e49211d780b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.4` - linux; amd64

```console
$ docker pull kibana@sha256:a8fe02bb0bd0f353c19f8827635e66f440c8fd778d44ef949a3f992afb546f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 MB (406391855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7553c079806ee53123924754cd51ea37e6ef99cd2863e01f63af44d085c6da32`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Feb 2025 12:46:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.build-date=2025-02-07T12:10:16.190Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4d74e2c041a2e9b7c6cefe20d106cde5f3d2439c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.4 org.opencontainers.image.created=2025-02-07T12:10:16.190Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4d74e2c041a2e9b7c6cefe20d106cde5f3d2439c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.4
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Feb 2025 12:46:24 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f827cf61ac70c52052c4f3b54d8f0b67779e22c3e9d6fbd249e791de3fcc4c0`  
		Last Modified: Tue, 11 Feb 2025 19:31:58 GMT  
		Size: 17.3 MB (17306447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f328f817319dc1f5b27eedba00ae6c31e644fdc5b8dad866487475dd0280110`  
		Last Modified: Tue, 11 Feb 2025 19:32:03 GMT  
		Size: 344.9 MB (344902137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadab65cbc0bb0fdb2a9437f06414461c182b5e9970637de804e237f1da10588`  
		Last Modified: Tue, 11 Feb 2025 19:31:58 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14be1294860db4cd0872dfd5479c5cdd2bef8101d5f5b780776a15538c7b8946`  
		Last Modified: Tue, 11 Feb 2025 19:31:58 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3729e291a047d83f3f4462b12a121e6990e5ece057de0203ae6c191474bbbe0e`  
		Last Modified: Tue, 11 Feb 2025 19:31:59 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c34b10fb41e66b96f23aae6272d81638e6682417aaf6656ec452d11df7947e7`  
		Last Modified: Tue, 11 Feb 2025 19:31:59 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5f29c374307b16a1ebeaa44659a53e9145fb87519a9f4497cfbc4276ec48e1`  
		Last Modified: Tue, 11 Feb 2025 19:31:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c182ba9a2c307b9f57558c489a40385948d827a3660fb006c94c5ad363380aff`  
		Last Modified: Tue, 11 Feb 2025 19:31:59 GMT  
		Size: 4.7 KB (4710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483accbd3d03738432650eb71c052b19b1509b4552ac5049cce68fdc0cc691b0`  
		Last Modified: Tue, 11 Feb 2025 19:32:00 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9912571b5617de1666a4ad28aee63487b4ee6f76f1e38e953a12f8eb7e74ae`  
		Last Modified: Tue, 11 Feb 2025 19:32:00 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3787cf5a6352085afd96f2907623c36c842840bafc48a2898b1c218ca6c5749a`  
		Last Modified: Tue, 11 Feb 2025 19:32:00 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.4` - unknown; unknown

```console
$ docker pull kibana@sha256:3a4b61393590aedd2bad6024d508a916069bfe301089aa940e38d836d2b2791d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da7b1a753d29e19b0629ef535d0a13f774b433417fd9bc77aebb9745cd87ec4`

```dockerfile
```

-	Layers:
	-	`sha256:3848060150f93c615459787278d1d102aafbf6726138b9a386cb171f80c33070`  
		Last Modified: Tue, 11 Feb 2025 19:31:58 GMT  
		Size: 4.3 MB (4302424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bec83950e1bae5e7ccc8bab8191a083763ab15f18236d0d3b4eaab478e8a5f1`  
		Last Modified: Tue, 11 Feb 2025 19:31:58 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e2de0ccefd27c478aad644b6b25982225d9df9ed7c4846944547c170edf25810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416161241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b08dc27b1d12ee8984b278ab491eec3b0269781e13badf1131b2c463100da5`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Feb 2025 12:46:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.build-date=2025-02-07T12:10:16.190Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4d74e2c041a2e9b7c6cefe20d106cde5f3d2439c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.4 org.opencontainers.image.created=2025-02-07T12:10:16.190Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4d74e2c041a2e9b7c6cefe20d106cde5f3d2439c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.4
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Feb 2025 12:46:24 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38feabab55bfd2933d1ec4b31e6e9b5e2a9ea42d56ae510dc78d3cee8a78ada3`  
		Last Modified: Tue, 11 Feb 2025 19:40:45 GMT  
		Size: 16.1 MB (16093679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147d52e5a369af0978d05fd938116592269986ff3b580f79c8bbeb921e675795`  
		Last Modified: Tue, 11 Feb 2025 19:40:51 GMT  
		Size: 357.4 MB (357427993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8518716115e478cf69debf7a4c1a54ff80a2d6cdea528fc483be3c2e31555a0`  
		Last Modified: Tue, 11 Feb 2025 19:40:44 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597d79e4c7eb14763d3c33f9a687f31acddd3035c2b858fca2baf56d0d6b5e3e`  
		Last Modified: Tue, 11 Feb 2025 19:40:44 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf595916f3db7497d5a054c9daabcb9e02a60cc49a07992f59590694eb1288b`  
		Last Modified: Tue, 11 Feb 2025 19:40:45 GMT  
		Size: 5.3 KB (5285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d75c9bf7c90a864e16cb85925fd277bfd441845ff4ca8ee5fe6ab00abca363`  
		Last Modified: Tue, 11 Feb 2025 19:40:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfbcfa0803b639b842bab2e7b89741fcc09cf249ca3286ec1e3b83817571d90`  
		Last Modified: Tue, 11 Feb 2025 19:40:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28079e6cea718891392b3cab75058861056a3e1104160dd66db29079450559fe`  
		Last Modified: Tue, 11 Feb 2025 19:40:46 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764829800873f4d1ef59c2b38a36caa8c3f0d07b4105fd06fa49146f3d38e59b`  
		Last Modified: Tue, 11 Feb 2025 19:40:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c9ceb884cf27357636afe25f74f6f627338a984280a02f69e1177a9653b90d`  
		Last Modified: Tue, 11 Feb 2025 19:40:47 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a854d3c13dce2ee712becc359d138e9bddc0e97a157ad8a6464ce407d1e264a2`  
		Last Modified: Tue, 11 Feb 2025 19:40:47 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.4` - unknown; unknown

```console
$ docker pull kibana@sha256:f813df4a3dfe9a5b059e80f06f96d4d703118754a45ba467d89e8cfef80de008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2606820673c8c8cd38f9b5e42655e3db5e63dc2f4da8bbf004c142b0a93a585a`

```dockerfile
```

-	Layers:
	-	`sha256:fd0d0ba8d7613aaa925174e16b79b4a7a62ce12309282795c342b38b609101ac`  
		Last Modified: Tue, 11 Feb 2025 19:40:44 GMT  
		Size: 4.3 MB (4302675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144066da6c77a981955d7321f0c422980f322cba063f36349d3c1bfde34881a2`  
		Last Modified: Tue, 11 Feb 2025 19:40:44 GMT  
		Size: 40.9 KB (40928 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.2`

```console
$ docker pull kibana@sha256:c6caadab69daa22ed0f812494fe6c84a1379dbc4b61e69d122fe1100df7d6c9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.2` - linux; amd64

```console
$ docker pull kibana@sha256:661b7d3e8a32acb82985d063d0f78b9f435246a045a6eddcf11564073cb94dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406707227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ca479907fc1a0892d8cdfd3507f1584ee06f15d62e9676018490a933bfd79`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Feb 2025 12:44:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.build-date=2025-02-05T19:17:29.251Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d7985c80643203de533d99844eb1b53cae85f8f9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.2 org.opencontainers.image.created=2025-02-05T19:17:29.251Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d7985c80643203de533d99844eb1b53cae85f8f9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.2
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Feb 2025 12:44:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e167dac9e7441a7f6927c9d5a0080605cd42f95ee2a430691c39e4b751f3519`  
		Last Modified: Tue, 11 Feb 2025 19:32:10 GMT  
		Size: 17.3 MB (17306351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b010f801b36a8b0ac980a31f6569d83da64db4c869f081a843c8ce94506a3c`  
		Last Modified: Tue, 11 Feb 2025 19:32:18 GMT  
		Size: 345.2 MB (345217626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c19c40b11961717ba31ecbd2cb3b81c4354101799bf4d4d6a2e198e6eb74fcf`  
		Last Modified: Tue, 11 Feb 2025 19:32:10 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83c00b515be17523ef68ff32ce56bca7f47c1775652f7b855763fc7398d3e21`  
		Last Modified: Tue, 11 Feb 2025 19:32:11 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f874dbe0f3dcef5c06cae69c98cb3fa5dd24e508a8e87815fb8d1928ef4f7539`  
		Last Modified: Tue, 11 Feb 2025 19:32:11 GMT  
		Size: 5.3 KB (5277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf00d4b124907267ed0f14346ba185c91c2ee0973a071a3a5b0489b53a69da`  
		Last Modified: Tue, 11 Feb 2025 19:32:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce808478d355b5a68025433c7542a2fa28b55adb7f4515d58b4959db896cb9f`  
		Last Modified: Tue, 11 Feb 2025 19:32:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95a5361db4d3bb7865f3d0e3a668516c505564df4e42ce874b577addb18c26`  
		Last Modified: Tue, 11 Feb 2025 19:32:12 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1524b4b4b09cbc617ed2e99f503f5cb65aa5b2acd8f7da207256e1a46ecf4e23`  
		Last Modified: Tue, 11 Feb 2025 19:32:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90164fdde954872e1571c5c7509783457316d88fcde302786a8175db3692ea4f`  
		Last Modified: Tue, 11 Feb 2025 19:32:13 GMT  
		Size: 189.4 KB (189431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81106e9e94e38f609b1f6b60f88df42a7143d98b51cc0eadfe8aab09e6622ff0`  
		Last Modified: Tue, 11 Feb 2025 19:32:13 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.2` - unknown; unknown

```console
$ docker pull kibana@sha256:982cb02eedf5ac7a20ed909ce8ad662b2d140af5ccffd45957e4e10c7df1a81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4437689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cd48c32606b98279c931e9c95a97275594a2470d7a2a9a1600586ec100a677`

```dockerfile
```

-	Layers:
	-	`sha256:07b6b1a7a1e4722244f79c538fc425d3bd1e444d103be67d8611f68c77e0596d`  
		Last Modified: Tue, 11 Feb 2025 19:32:10 GMT  
		Size: 4.4 MB (4397009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd1e73f4b183cc112afd4cde8428bc96c58de469aa33c20dd61240ea9cbb2308`  
		Last Modified: Tue, 11 Feb 2025 19:32:10 GMT  
		Size: 40.7 KB (40680 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e2178039f97ef48a2cfdaaeb5c755c18ac4cda9d84475d1439b30152daa63480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416156502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90d141fcdd928daa1614ca9826bad95cabf044bc97056b02a86a6c1791fe646`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Feb 2025 12:44:29 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.build-date=2025-02-05T19:17:29.251Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d7985c80643203de533d99844eb1b53cae85f8f9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.2 org.opencontainers.image.created=2025-02-05T19:17:29.251Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d7985c80643203de533d99844eb1b53cae85f8f9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.2
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Feb 2025 12:44:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38feabab55bfd2933d1ec4b31e6e9b5e2a9ea42d56ae510dc78d3cee8a78ada3`  
		Last Modified: Tue, 11 Feb 2025 19:40:45 GMT  
		Size: 16.1 MB (16093679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f45ebf0323d7d6c6bb5ecd0357848bc44905932672d0cdb695f2d413d3018d6`  
		Last Modified: Tue, 11 Feb 2025 19:47:39 GMT  
		Size: 357.4 MB (357423231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de76db1db2784b3570b7a97c125fee3caf80d856a35e74865e57df1947fedca`  
		Last Modified: Tue, 11 Feb 2025 19:47:28 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac08a000d1e9a6573ecf5d4c259b52220c3b88ba2fe0b2d770aebd993e60d4a0`  
		Last Modified: Tue, 11 Feb 2025 19:47:29 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c1209c8bdd1e1e27f83faad3cc3667dee2d76720bb39ac10772d777c3ca466`  
		Last Modified: Tue, 11 Feb 2025 19:47:29 GMT  
		Size: 5.3 KB (5281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426d2fd31c1400032acbb2647d9615b8741e3f3eef899a7b97979d3260f0775a`  
		Last Modified: Tue, 11 Feb 2025 19:47:29 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e952b1be9b54a28c2dc4d1d0b5477f52524c36fb805b2ee9a0cd7411b2c656`  
		Last Modified: Tue, 11 Feb 2025 19:47:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904a83d27b04be3e7eb556fcbaad8da6e2d0ecccaf48d43df7d77b6cdea458c3`  
		Last Modified: Tue, 11 Feb 2025 19:47:30 GMT  
		Size: 4.7 KB (4718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564094997028e5bd619012c4a71af878904c00b52bb46783e2d3c05f3071eb96`  
		Last Modified: Tue, 11 Feb 2025 19:47:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4237d6201ba7c7a8c5e418f5c6c43060c2e537e196c3150088746f066f64dc3c`  
		Last Modified: Tue, 11 Feb 2025 19:47:31 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54da35bb5d8a0ba6e5a1c48276971632924d09d7ede933716d43b421b131f0ef`  
		Last Modified: Tue, 11 Feb 2025 19:47:32 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.2` - unknown; unknown

```console
$ docker pull kibana@sha256:cf78caaa9e8129485521e1ff297692c5b532faf846a7e2594849565f70aad708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4438187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0f0846a894a870aacae57be1e0498feadb023363f0aff6075b02541ce39278`

```dockerfile
```

-	Layers:
	-	`sha256:9c638cef946079ef9c6c50dc2d353dc963d46c75e4f0116fcf6c463acab2cbee`  
		Last Modified: Tue, 11 Feb 2025 19:47:29 GMT  
		Size: 4.4 MB (4397260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5d75e6d1d9a4caa1d3e4e061175b72394960d158c3a21fd87081ef35a78d84`  
		Last Modified: Tue, 11 Feb 2025 19:47:28 GMT  
		Size: 40.9 KB (40927 bytes)  
		MIME: application/vnd.in-toto+json
