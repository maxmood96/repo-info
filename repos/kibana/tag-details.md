<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.20`](#kibana71720)
-	[`kibana:8.13.0`](#kibana8130)

## `kibana:7.17.20`

```console
$ docker pull kibana@sha256:cc537607c5a7ac4c7bf8f5e2a2028200460a35a3593de22196ffcc24009347bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.20` - linux; amd64

```console
$ docker pull kibana@sha256:165d6a0264843457a02cb6396bd9e4b16d679004b6fe27b1bc189f7cdad5632a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359689173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74351463330c90dd69081db440b67020a015c424b4c55b572fca415391210e71`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN fc-cache -v # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/kibana
# Tue, 09 Apr 2024 08:24:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T11:05:28.782Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=03253d4922979c94747a2f108370c00ad99df6d1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T11:05:28.782Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=03253d4922979c94747a2f108370c00ad99df6d1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 09 Apr 2024 08:24:48 GMT
USER kibana
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe144c362b194346e5dd02dfde53c63bee9f33e8645cba615b852e6826465e8`  
		Last Modified: Thu, 02 May 2024 00:54:13 GMT  
		Size: 10.7 MB (10705185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeac22a56d819e45da277a39a44a9ed9798ef5e394ca293929b6a8a6564c110`  
		Last Modified: Thu, 02 May 2024 00:54:12 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd30f5974e3c5e09a9d54f02c33389999f2edc5c4aab47b6247788f92aa2ef54`  
		Last Modified: Thu, 02 May 2024 00:54:12 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a37326c1989ba16a4fe47611e50c91a9123f4fae4d5476790d72ce8dc479a29`  
		Last Modified: Thu, 02 May 2024 00:54:14 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0aee2b8f51d984c5bc89870d8f25bc987a378099ffb45c7ac333f987efb77`  
		Last Modified: Thu, 02 May 2024 00:54:13 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c858d553a1d7dc6156232aebcfa604db6472263cb0b1f6301a54fc2e4145bab3`  
		Last Modified: Thu, 02 May 2024 00:55:21 GMT  
		Size: 304.8 MB (304800142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67f383fa3e4f71bbf46555026bf0facc1d0e9793fdc21a2f5792e943332534`  
		Last Modified: Thu, 02 May 2024 00:54:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9f20cf430fd13499d5ce412fbd66da108850ba9da40f4c98f54deea11e2068`  
		Last Modified: Thu, 02 May 2024 00:54:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d12605b547b80e079b982377ebcbd359d7bbc25d38969d1bbe4be4c62e526`  
		Last Modified: Thu, 02 May 2024 00:54:15 GMT  
		Size: 4.5 KB (4503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294777053dd63c59fe5054afefda0e8e1f1269a7c438c146528b325dec1a48c6`  
		Last Modified: Thu, 02 May 2024 00:54:15 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e636ab8a5c05d680e8cf3939b271c3166b4f9fa95899ff00394154f3fb447`  
		Last Modified: Thu, 02 May 2024 00:54:15 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab5371787921c30000d88e70378d09d971e767750660e64be106d10f06dd347`  
		Last Modified: Thu, 02 May 2024 00:54:16 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:70677c871aa90913ea76493cefb6141a8eb0dd2ff091be0e810f86f5094cced4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29110710a050c560036a074dee1711656451f320d30660a8d73b499207486c`

```dockerfile
```

-	Layers:
	-	`sha256:deed3babfc9d9324aff2f378f977de93af43babb351a6abf62cdb864f29c9087`  
		Last Modified: Thu, 02 May 2024 00:54:12 GMT  
		Size: 3.3 MB (3289966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efa31b1e2465775ee01d88e00a05dc0b8f3c7d222eba176aab8b94e83cf2d44`  
		Last Modified: Thu, 02 May 2024 00:54:12 GMT  
		Size: 44.4 KB (44367 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.20` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3331778057b65752b0a0dcb0d05817ef8f4db2da4005e51676bd3200a7aec187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370100486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a1e3238e91f59ddb89109947a8b9edd4a2a4ef91e311ee2ac1b66286712b29`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN fc-cache -v # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/kibana
# Tue, 09 Apr 2024 08:24:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.build-date=2024-04-08T11:05:28.782Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=03253d4922979c94747a2f108370c00ad99df6d1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.20 org.opencontainers.image.created=2024-04-08T11:05:28.782Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=03253d4922979c94747a2f108370c00ad99df6d1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.20
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 09 Apr 2024 08:24:48 GMT
USER kibana
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5d0d7c21ea60411e55b5523a8c2187d18bdec3a452c21708763f047bfb0ab`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 10.6 MB (10551305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18e95a4c15f82e6a2ac8d591656086912c243007fb37271b41c0b56b4acea9c`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186b8a3459f0195c0081dd1a0707dda8a8c2606672c2983a5c8aaf3c94965886`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fac697f917cf0cf446f4ee231c25c900de2df2e197c64cbf2fa49b9694286f`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ca2e6e15fcf3aff8c1472becdef226c9d51ab526713ff496da3141f45747`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4626e0a0198af26b57a536cba8d4b94adeba43d5065aa88b7f88ffcfd6d6055`  
		Last Modified: Thu, 02 May 2024 11:39:37 GMT  
		Size: 316.9 MB (316907928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d8739160ab495c753682fdd2550a2d7c0bf816a5d1220623e04737747c51d`  
		Last Modified: Thu, 02 May 2024 11:39:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccefee72870ece140c24d64339c9990f1899049d2129b22e0de893d898d8b408`  
		Last Modified: Thu, 02 May 2024 11:39:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03eea543ef6a0218eb8531ab3c40e399fe7e83df1c93bdf12c0f680e648949e`  
		Last Modified: Thu, 02 May 2024 11:39:30 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742078dbe42ebed9bf5006816ecfd9cc89c562b7dc491c81c080455376ffa91e`  
		Last Modified: Thu, 02 May 2024 11:39:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd6773c4f2bb7bc0ba0a6fa4feabda35bc679a19f306e638aedd38884a9b55`  
		Last Modified: Thu, 02 May 2024 11:35:12 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cddbb8cf0f12554d88b776019ae4aee0743f3de74d080416e776f879968be2`  
		Last Modified: Thu, 02 May 2024 11:39:31 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:d7e58394097712fd46166904a63c5e7ad2c5bb6be2305bc9a15aeb41447114fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de101a377295741b301236cb72e4f27201ad2be83ed203c0f7c3af6fc4be4d5b`

```dockerfile
```

-	Layers:
	-	`sha256:ef318d730f38c98daf56b94b0bd365abae8785bae56b713369582c3372e52adc`  
		Last Modified: Thu, 02 May 2024 11:39:30 GMT  
		Size: 3.3 MB (3290201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61cc0d8306eb4448e8a6704fadeae9ce4663629a8f34eba0d7564af0a2769866`  
		Last Modified: Thu, 02 May 2024 11:39:30 GMT  
		Size: 44.2 KB (44210 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.13.0`

```console
$ docker pull kibana@sha256:d713b80cdb02c0dd484de9bbbac2312e7dab98f09a25b6adbbfa30841649b828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.0` - linux; amd64

```console
$ docker pull kibana@sha256:d43324e676cbd2d2178a29057223bde6013dfee55d09d4ddba17e9013e78a6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.1 MB (375053138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c1f896185badaecfa762da47458d0a32f331944b16e7d985e9300b31ad9807`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Mar 2024 13:49:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T04:07:01.866Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T04:07:01.866Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9270f90453da34504c79124531d40b33decfcb048adc94ff1819d8570d7f72`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 10.7 MB (10705183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ee893e59a1a2d7fee8d90f81f61106159bc44e98327014963b7736bef51b92`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae1b253504a71c4529f6b2e7c1d5fcf256146fd64f282238c82c4b5ae998823`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeee51ecc63805a655f2ab121c976279751ce4472b50560b299fe84aee5dac1b`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2500363d16446137ed52467eae89732ac2ba2ef4f35740d9fbeb31fb76efbca`  
		Last Modified: Thu, 02 May 2024 00:54:40 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cb78aa516972699c3403452c24911660ce4c70b170093e660a9356af09455c`  
		Last Modified: Thu, 02 May 2024 00:54:44 GMT  
		Size: 320.2 MB (320164065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f065f373ad833ce464887751cf63c6b5d93ef1c4bc616ca70bdebcbb6fb5af97`  
		Last Modified: Thu, 02 May 2024 00:54:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fbb338f026b9e8e7b987fce14b56690a496894ff8777430684f6b8bcb748f5`  
		Last Modified: Thu, 02 May 2024 00:54:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f21d8fb616536b5c54722ba30fed6d5f02b7085ff7294987a7e0ca1c7fd80`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 4.6 KB (4563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7499fcd7ec800bb3cd3cc4072492a6639d91a7f6ee3a2027127c0e5ffe13b65d`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd916f8c3f7f388d2bd0444c3d92a2e88d80d6ed7bac2583fa9a2dc26ee641b6`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c5146376b1e2cabcb6d6298abd9bf983b472e29b0f5962a77092c2936a33d`  
		Last Modified: Thu, 02 May 2024 00:54:41 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:c782351cef46b06a4dbfd40a76d825a75a7f929dddbcaeea8c13b0a98555a81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0465541209b81d0c3e557ee48adca5bccda750eed990876c97086518fa6c57b5`

```dockerfile
```

-	Layers:
	-	`sha256:63babf3416dc9d0d0ba89165b5228055bd7b66edf93a650d21f1b928b1673644`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 3.7 MB (3749657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f500da12478a9dcff4a04969877344e3db799d8f543f98f4b9640cd8d717002`  
		Last Modified: Thu, 02 May 2024 00:54:39 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9dfc2e86ca0e4a7528ef632844456774bf787f9870036017e235ada77408c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385487015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0fe852981d370c7eb7db96c5990336fb44c723062458b5b6e86a49d8db9b2c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Mar 2024 13:49:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.build-date=2024-03-22T04:07:01.866Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.13.0 org.opencontainers.image.created=2024-03-22T04:07:01.866Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2e3a5cd43e835baa1d596b1aa54735992259ecb9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.13.0
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f5d0d7c21ea60411e55b5523a8c2187d18bdec3a452c21708763f047bfb0ab`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 10.6 MB (10551305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18e95a4c15f82e6a2ac8d591656086912c243007fb37271b41c0b56b4acea9c`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186b8a3459f0195c0081dd1a0707dda8a8c2606672c2983a5c8aaf3c94965886`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fac697f917cf0cf446f4ee231c25c900de2df2e197c64cbf2fa49b9694286f`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c0ca2e6e15fcf3aff8c1472becdef226c9d51ab526713ff496da3141f45747`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 5.3 KB (5295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c55329d5b58905918d9c2d6aa17a2d52e864271b6e89b77dd6aa95b7102f72`  
		Last Modified: Thu, 02 May 2024 11:35:17 GMT  
		Size: 332.3 MB (332294389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed089e73d0dfc0bdc9b35ae240b644b4b8c2e5a5054eeaba1c951f4056442c57`  
		Last Modified: Thu, 02 May 2024 11:35:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3e6ae72d42eb86957f8cb3e4f57276a82bf37cc1899bdac8ba07ae88971340`  
		Last Modified: Thu, 02 May 2024 11:35:10 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81b1007d14653d31f4c62bc30f0d8004be33697d5d67efc67fd0a37941c857b`  
		Last Modified: Thu, 02 May 2024 11:35:11 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0a75345761143d942361dd5e6fc02d1c5b23c41ea7ae81671b7db90517974b`  
		Last Modified: Thu, 02 May 2024 11:35:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd6773c4f2bb7bc0ba0a6fa4feabda35bc679a19f306e638aedd38884a9b55`  
		Last Modified: Thu, 02 May 2024 11:35:12 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7011dcb4f45a13db5835a2caadac9c2a860e1f2f4dc467e68b892c1b35d13a61`  
		Last Modified: Thu, 02 May 2024 11:35:12 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:12b10d082822f3225367a549b65c7b6f99034a845f789d30bd376b6c66f40050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8a5866c3c54fb0f8d64be40e18bbb6060348b50616faa3b6e93b9107296912`

```dockerfile
```

-	Layers:
	-	`sha256:22ba0cfeb662c7bf269170a6c4f87242d1346f8c74ea8de706f002d84470947d`  
		Last Modified: Thu, 02 May 2024 11:35:09 GMT  
		Size: 3.7 MB (3749892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44e66ceb8c4bb894e0859e6b8077d4c0a19d76eb6eec07bce0237b1e78b775e`  
		Last Modified: Thu, 02 May 2024 11:35:08 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json
