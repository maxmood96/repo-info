<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.8`](#kibana8198)
-	[`kibana:9.1.8`](#kibana918)
-	[`kibana:9.2.2`](#kibana922)

## `kibana:7.17.29`

```console
$ docker pull kibana@sha256:214fd19f90efd750940e1269ec992f254b641c78b9d8af2a184f84cd4e69daca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.29` - linux; amd64

```console
$ docker pull kibana@sha256:c0aa33485941239d163f432b239d3a02f4df8626f45b39b0637290313baab979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353913008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdd23f0c4a7707dd255886269010b1e12cfbcb4323108633a4dec4424bc098c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:28:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Nov 2025 23:28:28 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:28:28 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Nov 2025 23:28:28 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:32:15 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:32:15 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:32:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 13 Nov 2025 23:32:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:32:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:32:16 GMT
USER kibana
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdb63166b01065b5f7b99b6c9aef0b064c2619c8a8d2aa28900c35620dad640`  
		Last Modified: Thu, 13 Nov 2025 23:33:06 GMT  
		Size: 9.4 MB (9432171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e243fbaf8e56d5b355b644529d3ed4788c625a92dbbbed24fdb160ca65e1a`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49d4ff80eb1fe4f3116402fc8f8b14f01dd2667c426dd0c6ba3a71ed0a4f7ae`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48405d79663978c1cf545837462f1c20b1c07ad7bf145101b7627051b2bc13d8`  
		Last Modified: Thu, 13 Nov 2025 23:33:06 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aa325ed52e36638eeeb312d4f855b884465eb853383b69373091f002014281`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e171d897aa16a8798e29bab0abcec849131cd946dc34713709b638e7c904ae`  
		Last Modified: Fri, 14 Nov 2025 03:16:12 GMT  
		Size: 298.1 MB (298112553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd272ceee08e890fbedfc09bf4dd061bbc4cdbb94d8a97ecdc2026c1ea650c5`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9ab140f6e2dfdf61227617e6a235aa453a7a3f6495115ae02e6fd77406f46`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5b9c0f18f07e84fb9334b4b92b4c3c56b4fd1cf8fa909b539c13b757e88328`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8f438b26057468d57ceec2555726a6b4dedb5198d5a72fc8c9ecd062a05e7`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1b7f1c0d124847f7c8bd31f3a70c1960fffbc81978dca5f157529e7ae128a8`  
		Last Modified: Thu, 13 Nov 2025 23:33:06 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718e8bc690f6e59d6eed6bf905a7b0b1f518eea1b038ab980ac727f64a813b6`  
		Last Modified: Thu, 13 Nov 2025 23:33:05 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.29` - unknown; unknown

```console
$ docker pull kibana@sha256:4fa9431b42decd61b978c094b1f5167968be0f3cd93303006765164e1eb49fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070f1f745153a061d784200168e4aa7e45a1cc2c84a72c951a3c90a273eb4e3b`

```dockerfile
```

-	Layers:
	-	`sha256:cdfa6528661e2f127de796a7ebba4c0bde44c8f21f0e9b1134614821f5132474`  
		Last Modified: Fri, 14 Nov 2025 03:11:42 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fbad5574700428d9e57e578aa8dce94626a1457e6016765d503452d6e2e899`  
		Last Modified: Fri, 14 Nov 2025 03:11:43 GMT  
		Size: 44.5 KB (44511 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.29` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3304b1b08cd54106bb61c533d80cb4ac4d8ca905abe5351e6eaf1792e8f27762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366095962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be02998de38651cfc11fe55dda0c3b10ea8d6d31ee19df52bf76301cecf9227b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:35 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:27:35 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:27:35 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Nov 2025 23:27:36 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Nov 2025 23:27:37 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:30:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:30:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:30:52 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:30:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:30:53 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 13 Nov 2025 23:30:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:30:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:30:53 GMT
USER kibana
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6397d3511035aaa5996ddbd63c844242cdf265782c4d0652b67548aa3fef509a`  
		Last Modified: Thu, 13 Nov 2025 23:32:03 GMT  
		Size: 9.4 MB (9446173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1853a381f41232f921e5526c3e6700154b827f6949ce80249b881bc6d699cd09`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a760837544bebe14a33bb967a1935d4a4d15c3abb9227281080d71dbe975e53`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922bd60bd5fec7692b52505f3a4906334bcbb68e40c63f2ec9e47f2af918012`  
		Last Modified: Thu, 13 Nov 2025 23:31:51 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89931a8edb2c8dbee44c71f14803f8136f4ec18de1703d9337b4641620485f85`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf67254e8331c96e4c2f96142859368e57085c91814b2f0e300934367be2c05`  
		Last Modified: Fri, 14 Nov 2025 03:15:36 GMT  
		Size: 311.1 MB (311148121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55926e73b726f9b587823eac64e2486adf2c4bc7eaaf0dc86a1823587916f465`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f1fee166071308bd9f88d3a9c288789bb822f58d513126237e97547bfffb71`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12355655218fe6c3b48187926fe316193619b4b7b9eae9eab2d102d577d00a30`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a729783706fcbd9ef444378dee2624e0fffa33a4213baa8a774ff08d00b3d2`  
		Last Modified: Thu, 13 Nov 2025 23:32:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3565fad2095d35954b8261412110b44af400bcd11be235b398ae7faf5599bc`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54760310f932ac7c65ec67da5c9eb6f576c221ed4872eb417a199ea2a76978`  
		Last Modified: Thu, 13 Nov 2025 23:31:50 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.29` - unknown; unknown

```console
$ docker pull kibana@sha256:8439078a15410074229ad08b9ed26610f0bd8aa625c8448dd6c283f751be204b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7a100c42b2ea8ceae595e317296dd281ae632807f3d9ecb9cfab35ee560c8`

```dockerfile
```

-	Layers:
	-	`sha256:fdcf66b35195edd1229f8daea36f16ec924ae474f9c9f5d639b1d96a824583e8`  
		Last Modified: Fri, 14 Nov 2025 03:11:48 GMT  
		Size: 3.5 MB (3507898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee98450ea19b52544a490c084455349bf886d683fc7244bef3585fb42d8c9cf`  
		Last Modified: Fri, 14 Nov 2025 03:11:49 GMT  
		Size: 44.8 KB (44789 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.8`

```console
$ docker pull kibana@sha256:4c73f1e8fd61baad0716c71dfedba2194ed909300560ad66ab8251bd7f11ba94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.8` - linux; amd64

```console
$ docker pull kibana@sha256:d7c4b9662d957cd41fcfb32c554cd7c25557899511fb09926fa28156bcf77ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424079670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb990441cddf3619a69ce486f938576316aab79cf986845612b20f00e41d4df1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:34 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:28:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:36:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:36:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:36:54 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:36:55 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:36:55 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:36:55 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:36:55 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:36:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:36:56 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:36:56 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:36:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:36:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:36:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa7e3f5276d9a52d6abe8527fe00e8cb71ba993e041bcd1c37db82c8565f62`  
		Last Modified: Thu, 13 Nov 2025 23:38:07 GMT  
		Size: 9.4 MB (9432182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb566056a2f72f3c0d36be7a38997b8d1d6462fa0ec8fcd234041db225389c`  
		Last Modified: Fri, 14 Nov 2025 03:17:15 GMT  
		Size: 368.3 MB (368279132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddec7aebe1d1a4de4d26a7d08e1a2884cddaaad30f12908c9f66aea29148e344`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14ea6f6f4524247905656484936f3bba1a49c33d1360378e554c90512d922df`  
		Last Modified: Thu, 13 Nov 2025 23:38:08 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1887c4ab1d067a93261b962ac9fc4ee3820741c138017f89775ba504c0c4a`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be88165050c540019b55dcb3913d33e928cdee0c4950798c1cf7d4f067d6d7e`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47beb95e0935f6cd8b92bf84d7fcb59013455e99af72163cce89e37f559ef66`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e29c2f534b0713ae1eec9e185d5ffecdf40705e8627f6ca30fc1ccaab92ca3`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 4.8 KB (4768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3768e40446a0706b1d9c9f95a34b73f1b6453918f88b905d5799df0d5c600ac9`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d1815f836fc48b66044cc1656e343143eb66fbe43e74d8dc8d4f7908b2233f`  
		Last Modified: Thu, 13 Nov 2025 23:38:06 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf42b8285681325cd51e1d6daff0127a6c5590674382b14d5242e9a185648b8f`  
		Last Modified: Thu, 13 Nov 2025 23:38:10 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:903053e21ac27118b9c5b77612c4294c83d9260bf49800b978739d34ac05c329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db160e71d7afcdf8ed587c1bd01a7ee260c511a6b8b4279380bb10a3f20494ae`

```dockerfile
```

-	Layers:
	-	`sha256:ac2feab0794231218fd3bf52afbe2cb6f36e64a50adb2439190bd1a04bc4dfe2`  
		Last Modified: Fri, 14 Nov 2025 03:11:52 GMT  
		Size: 4.9 MB (4856890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30130bbfba23015d367d7aeab62a8d79e080423b3f708b6eaad4cfa1d184bd66`  
		Last Modified: Fri, 14 Nov 2025 03:11:53 GMT  
		Size: 40.7 KB (40684 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a8c795e0a6448f4112b26df31eab623d233f5d55c2dc9070df3c3313532ad6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.4 MB (436355230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f4e07683e123e4f95f04229e7bbc0322ad90a09a67c5186cdc0cf1cbb4c0f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:27:46 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:27:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:34:43 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:34:44 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:34:44 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:34:44 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:34:44 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:34:45 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:34:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:34:46 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:34:46 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Thu, 13 Nov 2025 23:34:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:34:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:34:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de63df616becf613cf5fe961e187fc6129aa4b6d1b5509db6b1df0c8855a7a7`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 9.4 MB (9446139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c090a108fe140a15dedec5955270529bff007c1f1c9a79677aa83379c3f4b780`  
		Last Modified: Fri, 14 Nov 2025 03:16:43 GMT  
		Size: 381.4 MB (381407353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7addf77df7fe3204f04de322cf7ea86b59e69c8aa9e26fd50a7d9029226be5`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a65f8bbd7e9d95181ae79ffd18b90a44d166c7025a2325e93eb0488cce6d6c`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8eb30e0d24f5bd8f1e55fa2c70d40abeb3433cf53b0fd561aaf5070fe43193`  
		Last Modified: Thu, 13 Nov 2025 23:36:01 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410b06427c0b5cd07cc2eea851aa0bc7da593c1a21c9c9d673677c9867b1bca5`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cfd7eb4342b3ebb07a436bc7eabb448cfb63b08af09ff8a2a17f506f43da25`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7486155002a8e617ffd5b2f54347df258b3acb32f2c6530e0781d42c4fae35`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba29ab01d8b73367d63e6ad72b76b69fc579d73b09a2b157e9c559c2a4389`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e8d5b05c91bf573a0a0ab1ff3ac21ec59e16c1c610d4f760e59c7ae083801`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87df0fbd969ca87b03ee7923e2deb35235ebdf8c4094c4ebc4df8817e742d069`  
		Last Modified: Thu, 13 Nov 2025 23:36:02 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:41ef8b811dd035e7a1e850902ee962a8c3fe964f8357cc5fb691331bc1f749f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4898884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a87c03b89fd13cfbb2670177deec5a6271f3e0ffc05f2b13e14a0d47e8c036`

```dockerfile
```

-	Layers:
	-	`sha256:85181590cdcb3a32a258d062299c54dacc57f14065bb67bf603805a639544277`  
		Last Modified: Fri, 14 Nov 2025 03:11:58 GMT  
		Size: 4.9 MB (4857954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1dcf166553967c58eae09a06b1350bc953ba549467c61d69fd22deca57c029`  
		Last Modified: Fri, 14 Nov 2025 03:11:59 GMT  
		Size: 40.9 KB (40930 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.8`

```console
$ docker pull kibana@sha256:bddcf61efe5b45dc178aef7f3e17965bce61eecd79127a7d3ce2dae5ba8281d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.8` - linux; amd64

```console
$ docker pull kibana@sha256:da8c977535e587949c61c13d080a6aeb4a748692066ee6deb2eddc80210875fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438430688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af2cb3531af182a3be10c048260e1d494c3621fc98337d6c122cfa659404e2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 18:16:41 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Dec 2025 18:16:41 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:25:22 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Dec 2025 18:25:23 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 18:25:23 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Dec 2025 18:25:23 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Dec 2025 18:25:23 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Dec 2025 18:25:23 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Dec 2025 18:25:23 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:25:23 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:25:23 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Dec 2025 18:25:23 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Dec 2025 18:25:25 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Dec 2025 18:25:25 GMT
LABEL org.label-schema.build-date=2025-11-26T23:15:37.360Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5f55be16d833f6df054715d37659874bcecaa0b1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.8 org.opencontainers.image.created=2025-11-26T23:15:37.360Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5f55be16d833f6df054715d37659874bcecaa0b1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.8
# Tue, 02 Dec 2025 18:25:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Dec 2025 18:25:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Dec 2025 18:25:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed621714688a170958a8a00a01592a8c90426a4007f4a3f35662f96cf471fff8`  
		Last Modified: Tue, 02 Dec 2025 18:26:35 GMT  
		Size: 9.4 MB (9432150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09583be25bd212aa4ee114598161dd15fdf3c1f5aff41b80cd698a1462c3c101`  
		Last Modified: Tue, 02 Dec 2025 20:06:13 GMT  
		Size: 382.6 MB (382630110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9fb302c87b80072f3ec06fcb40f0a73c7213ba2a02ddd4c1a041f7dd970b94`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e292c84917cf28a6957c346995b70e4f62218a587e14557a570c0218a58a5fd`  
		Last Modified: Tue, 02 Dec 2025 18:26:35 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447705bbc811bffef55de2037efff3e302f737d28415d6324072483681895536`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84455764b27ab298adfc4894b8b2ae36a515aac0b16f373cb2c352657eee506`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fc0dafe8e7ca83918bf1b5f5e45ac21998dfe22b49fc7f8241d550d808ccf4`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967aab3ba31655d1ad100351a29300d81ccbe4f90b676111c21de48f7ed33e8e`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7228ac670d69a3e8c74546ee84c5d132a0c18904f3e92bb18e15c5588ba04a`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374c525a0db4bcd9caa7baf509c962b23c5ac6b3da6c6ee7793defa4743371d6`  
		Last Modified: Tue, 02 Dec 2025 18:26:34 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5810bb0b4b9bba0d3d486d8ca00bb2d665ff380640af8c1c70a98d867bccea`  
		Last Modified: Tue, 02 Dec 2025 18:26:36 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.8` - unknown; unknown

```console
$ docker pull kibana@sha256:396064852db7a7d074e12bf52c78dfc84084eb09a99e7c9ef4ba9e3f58c303f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fee7527e5fb1a0ede709dedcf2defaf9deac8185d4709ea6db0bcf8a628a4d2`

```dockerfile
```

-	Layers:
	-	`sha256:d477e7fc5d6b3d58ce52a95fe90266bb1267309120f2f80daa33dfd0015fcb18`  
		Last Modified: Tue, 02 Dec 2025 21:11:24 GMT  
		Size: 4.9 MB (4921231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46d5fe23567f7b8fc9cb71c8e18c4b6a9e3c12c41ce68a293c8aac731e586dc7`  
		Last Modified: Tue, 02 Dec 2025 21:11:25 GMT  
		Size: 40.9 KB (40908 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:571ae60f8b9b5686541ba0dde882bac060dddc23e30e2040c9b41d8814af27d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 MB (450603548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3db9b782201295458937c96b2d658081f3e174def18883d9aba26dcb294815a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 18:19:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Dec 2025 18:19:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 18:26:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Dec 2025 18:26:05 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 18:26:05 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Dec 2025 18:26:05 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Dec 2025 18:26:05 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Dec 2025 18:26:05 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Dec 2025 18:26:05 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:26:05 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:26:05 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Dec 2025 18:26:05 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:26:06 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Dec 2025 18:26:07 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Dec 2025 18:26:07 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Dec 2025 18:26:07 GMT
LABEL org.label-schema.build-date=2025-11-26T23:15:37.360Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5f55be16d833f6df054715d37659874bcecaa0b1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.8 org.opencontainers.image.created=2025-11-26T23:15:37.360Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5f55be16d833f6df054715d37659874bcecaa0b1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.8
# Tue, 02 Dec 2025 18:26:07 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Dec 2025 18:26:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Dec 2025 18:26:07 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f981cee656bc646476a71843af5bdc141d9ea8ae69d987607f71d2ab0506fd7`  
		Last Modified: Tue, 02 Dec 2025 18:27:27 GMT  
		Size: 9.4 MB (9446227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ba2df8ad763873b8828b992607f89e4e32baf672acdc1e1ea7785c9abf365c`  
		Last Modified: Tue, 02 Dec 2025 19:59:50 GMT  
		Size: 395.7 MB (395655525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c1a8b84682cdb476dc717f15960c5a0114fe6b5f883c78fffdb74a30b09e33`  
		Last Modified: Tue, 02 Dec 2025 18:27:25 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934200382a96a3c27e5018045fa7f3cdb60bf161259eafe7de2bb1c25551efe5`  
		Last Modified: Tue, 02 Dec 2025 18:27:28 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8237862a6762a7e02b63503ff6fdfcec64301535102946fec722bc9e9a71b158`  
		Last Modified: Tue, 02 Dec 2025 18:27:25 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f805cacc8ccc30d26b3524a888bf20618b9117ea9fb8d122a5563727a6a286d3`  
		Last Modified: Tue, 02 Dec 2025 18:27:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791e58ffab6c3cdfe90436cc295cc26ad65c65ef51e879c12ad1fd477d90bbc7`  
		Last Modified: Tue, 02 Dec 2025 18:27:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b02bd36fbcb3f6d4b94280cd5d97e47fb67d6f5d4cfea63dea760503210ce5`  
		Last Modified: Tue, 02 Dec 2025 18:27:26 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab3ea264a46c885ab057cf779c363834eb5ffe9346fb520ac4721024a8be36b`  
		Last Modified: Tue, 02 Dec 2025 18:27:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2052493c1015e010e95ffd2c922736a636020ba417706ff91584b3badb4502f0`  
		Last Modified: Tue, 02 Dec 2025 18:27:26 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76cee911e50b3cbef869ab359818c68c76660106ffc2cbe84908df63afeff7a`  
		Last Modified: Tue, 02 Dec 2025 18:27:26 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.8` - unknown; unknown

```console
$ docker pull kibana@sha256:a11fea32be3d6b4a0dd65aced2ca1a7d5ef9183f0886d6e0d59639d7cf8b0f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5286296ea3f1847dd78c03b9f327dc112837b859c19e0af66bc557e87ebb55c`

```dockerfile
```

-	Layers:
	-	`sha256:1f436b2e6b4fbb8636c620917e775e15774ff3030728754d40c36b033a810808`  
		Last Modified: Tue, 02 Dec 2025 21:11:34 GMT  
		Size: 4.9 MB (4922295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93eb9ec97ae6c7e9fc9d1daab2f9b062d19e19e236a53a53ce8f0e3b9494e842`  
		Last Modified: Tue, 02 Dec 2025 21:11:35 GMT  
		Size: 41.2 KB (41156 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.8`

```console
$ docker pull kibana@sha256:ff478204277a7e25b27b99d83ed44cdc3b8a3cc33119866b55c314115bf9a7e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.8` - linux; amd64

```console
$ docker pull kibana@sha256:553fcefa9e1d34122160ac71983d51368f1592585da683bedad75574e2a48277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.6 MB (439565057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108cfe17c0459968ed0f73248c3409017ff4902e416d036b4576c75779964727`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 18:16:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Dec 2025 18:16:34 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Dec 2025 18:25:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:25:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:25:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Dec 2025 18:25:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:25:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Dec 2025 18:25:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Dec 2025 18:25:26 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Dec 2025 18:25:26 GMT
LABEL org.label-schema.build-date=2025-11-26T17:31:50.353Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6ecd757760927423daa344d901e634b43497e16d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.8 org.opencontainers.image.created=2025-11-26T17:31:50.353Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6ecd757760927423daa344d901e634b43497e16d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.8
# Tue, 02 Dec 2025 18:25:26 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Dec 2025 18:25:26 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 18:25:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Dec 2025 18:25:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Dec 2025 18:25:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d02f51cf745681bd07eb5fee7d7e6c85a72dd2d4509586d9a0b1f1a1f16d93`  
		Last Modified: Tue, 02 Dec 2025 18:26:46 GMT  
		Size: 19.5 MB (19535576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cdcd2618c3d6b47c1fab30ef3aa62ad942e15e6ef4988f33a95c74d16d33a2`  
		Last Modified: Tue, 02 Dec 2025 21:30:34 GMT  
		Size: 363.4 MB (363431175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17caf8ef025146fb3ea5576c32c64d4c3066b899052939580641f6e3bfadb947`  
		Last Modified: Tue, 02 Dec 2025 18:26:45 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c1d7e08718b6d4fe4a2f5c50b17c7a4fad096bdbabb48b72c5590e8ffa03aa`  
		Last Modified: Tue, 02 Dec 2025 18:26:49 GMT  
		Size: 16.5 MB (16460482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ff3041787d78a66332a7d8134761d6bde79b5eda352346f23d800d06bc4750`  
		Last Modified: Tue, 02 Dec 2025 18:26:45 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6ce42bdc20a862a42b161465c84fc75948d005426f17b8cb180cb61e54ebcc`  
		Last Modified: Tue, 02 Dec 2025 18:26:45 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc3555915942d9ff19ac510318651239a2f6e1a91b4366f4904c18596eca61`  
		Last Modified: Tue, 02 Dec 2025 18:26:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b149659e24484cf1827aee1cfa82c8a9273053d9f0098652bd9aee83d2eb8380`  
		Last Modified: Tue, 02 Dec 2025 18:26:45 GMT  
		Size: 4.7 KB (4741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9665e01762ed9d9e9876ced4447e105fca320eb1a7716cdecda4b4f309805bb`  
		Last Modified: Tue, 02 Dec 2025 18:26:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4404d869c7f1f3060240e55ec41cbb318cdaab1c8c9348361a13ea073208735f`  
		Last Modified: Tue, 02 Dec 2025 18:26:46 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb417c3aaa3d14a1efdbb35155bb3369afbc9fe78a42d74f053f5cba7dfaa2a3`  
		Last Modified: Tue, 02 Dec 2025 19:16:12 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dce340b0ef9b4f494ba3b9443389b8608e53e82a66eb267bff771caa97ecae`  
		Last Modified: Tue, 02 Dec 2025 18:26:46 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.8` - unknown; unknown

```console
$ docker pull kibana@sha256:e57181acbdc144d47a98ac94b6687d25f080f7afbb548bd198a9ad7e32a1df41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5747023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1dd7005328af1d0bf3da30d1c6d16318e6bcb9e38dec6f76702ef038af6e90`

```dockerfile
```

-	Layers:
	-	`sha256:be7bd9b840677a92871be7f4c9bf986e245a6866a27895cbe1ee5284a5338d25`  
		Last Modified: Tue, 02 Dec 2025 21:11:34 GMT  
		Size: 5.7 MB (5703797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9028b4c2b761f48ab9fa955ab864ac919807fc443d50b256764f988f024cd615`  
		Last Modified: Tue, 02 Dec 2025 21:11:34 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:837f3147afa022f726e5a67e1c9063fe62578801efac81185215328a76c00e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.7 MB (450741090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5385c720b5ccbbab6fd72c5f67f934198d6328e21e3ef8eb02e95abe07c6c5b0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 18:19:15 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Dec 2025 18:19:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Dec 2025 18:26:15 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:26:15 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:26:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:26:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Dec 2025 18:26:17 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Dec 2025 18:26:17 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Dec 2025 18:26:17 GMT
LABEL org.label-schema.build-date=2025-11-26T17:31:50.353Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6ecd757760927423daa344d901e634b43497e16d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.8 org.opencontainers.image.created=2025-11-26T17:31:50.353Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6ecd757760927423daa344d901e634b43497e16d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.8
# Tue, 02 Dec 2025 18:26:17 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Dec 2025 18:26:17 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 18:26:17 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Dec 2025 18:26:17 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Dec 2025 18:26:17 GMT
USER 1000
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161b5ecd42ca09cf23b7f8eb6b8f0fa073ce399aabced890d7f4f07c12c62f3`  
		Last Modified: Tue, 02 Dec 2025 18:27:41 GMT  
		Size: 19.5 MB (19494903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a240789da4f33613f82ecec202f26b06510f0d9b84dd0a5e88bcac0b94893fd`  
		Last Modified: Tue, 02 Dec 2025 18:27:31 GMT  
		Size: 376.5 MB (376467781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6926d023a2df4d79068bc155a72bf2f9272601ffe072cae26f4c2666f9b92b9`  
		Last Modified: Tue, 02 Dec 2025 18:27:37 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3323b9c324129e548d6583ea57c70aaf39d66732f4fe1015e9fbebd2838b3f76`  
		Last Modified: Tue, 02 Dec 2025 18:27:39 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fe1d39703b64ae858372f5eaa6a17dc660eccb15aa20bb85c1850292c8d0f7`  
		Last Modified: Tue, 02 Dec 2025 18:27:37 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae99f3366fa227b8d6fd0a2696950f44c434dba88fef2d4490a076f6ab92c9b4`  
		Last Modified: Tue, 02 Dec 2025 18:27:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd889c82245919e98b647c7191a70349e2ae43839980639dd325f8f2bd0dfeca`  
		Last Modified: Tue, 02 Dec 2025 18:27:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b82a65be7d02e3ab157560a3c65ecd807210b1e2de9700cc16317e563f790bd`  
		Last Modified: Tue, 02 Dec 2025 18:27:38 GMT  
		Size: 4.7 KB (4741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b308c5b9df75386777a646edff98bd05067ea2b6bc52a8293120f41cb3f296`  
		Last Modified: Tue, 02 Dec 2025 18:27:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228464c096cdc8c2d6fc077674fa17b8e1e13a567f979691ebe464843c63e9eb`  
		Last Modified: Tue, 02 Dec 2025 18:27:38 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc0b1559ac27f4f0212169be84fbae9c9c5a095295756c959165b3a8daa9e1a`  
		Last Modified: Tue, 02 Dec 2025 18:27:38 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f3359fd8633c61af3a6ac0aab1c4a0fc7c9632e508cc9d3fed6e102476749f`  
		Last Modified: Tue, 02 Dec 2025 18:27:38 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.8` - unknown; unknown

```console
$ docker pull kibana@sha256:b29461ffbdeed8254e3dc1429b91d0d6a601cb807d7b6632f340e2924ed9ee9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5745956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51337c4bf06e236879286cf35b72a37415e27ca2f327ec95aff83c5651d6f48f`

```dockerfile
```

-	Layers:
	-	`sha256:39da0db517e096ffc96f2d2066a969a43ca8a4e598d2be7eabd79d3edea5fcdc`  
		Last Modified: Tue, 02 Dec 2025 21:11:40 GMT  
		Size: 5.7 MB (5702473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b59f69d14b3e6d398d31c2c34dbef6cd448356a026fb9507e8dd0ccba9eea2`  
		Last Modified: Tue, 02 Dec 2025 21:11:41 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.2`

```console
$ docker pull kibana@sha256:1fcd6778bef458b725b98c57221b86842edba828a585fd26392ec37c67428997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.2` - linux; amd64

```console
$ docker pull kibana@sha256:5f945915c003957969f7dbe0c22e92819e14a31ecf2a9c828bc087f61cfb5a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.8 MB (444811175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8210c2b30eb78e34ad1fe0047a93f58ac4c5b50c2a73cc7264e31ddf065bb13`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 18:17:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Dec 2025 18:17:34 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Dec 2025 18:26:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Dec 2025 18:26:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:26:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:26:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Dec 2025 18:26:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:26:15 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Dec 2025 18:26:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Dec 2025 18:26:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Dec 2025 18:26:16 GMT
LABEL org.label-schema.build-date=2025-11-27T09:37:18.054Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c0340ed35c591c77a90ebf1c790c20aa07571672 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.2 org.opencontainers.image.created=2025-11-27T09:37:18.054Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c0340ed35c591c77a90ebf1c790c20aa07571672 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.2
# Tue, 02 Dec 2025 18:26:16 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Dec 2025 18:26:16 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 18:26:16 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Dec 2025 18:26:16 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Dec 2025 18:26:16 GMT
USER 1000
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92eb9ea7143693f1415fb8ceaf59998bfd7d624dd08d1c3726fa6f687de374ec`  
		Last Modified: Tue, 02 Dec 2025 18:27:36 GMT  
		Size: 19.5 MB (19535730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f2163f581e1e015f9a75aa3a85d167e002d6cf31ac2de71adc3036114e5393`  
		Last Modified: Tue, 02 Dec 2025 21:23:37 GMT  
		Size: 368.7 MB (368676976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38513f7012166ab4e380cabff16764e7546ded062d45c7e653d7c621f9286c9f`  
		Last Modified: Tue, 02 Dec 2025 18:27:31 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b325ff82519b280336709eaf05d130fc5aea132a869444e87b67e285385c4cf3`  
		Last Modified: Tue, 02 Dec 2025 18:27:35 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e11e695dce450bb4c5f9dbe9455a72a55a6c2a22ab6aaa136dcaec6c179978a`  
		Last Modified: Tue, 02 Dec 2025 18:27:31 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f238f9c4bdc3967396c5d5cd3ad67264a8954e2a5bbe4f363afacc147085d3`  
		Last Modified: Tue, 02 Dec 2025 18:27:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132fed661c3bccf8d180f687b5182ccc0de1b559db1db68d80a48488c4786aa9`  
		Last Modified: Tue, 02 Dec 2025 18:27:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d0e4ebb5ed8ecc19491168207c8449d892dd7a6f64e9ab3a193425cb605516`  
		Last Modified: Tue, 02 Dec 2025 18:27:33 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9febe82deb5b1e6cce0d2383a45c2572eaa169ccfa7ca46f0e5dfa2aa661b604`  
		Last Modified: Tue, 02 Dec 2025 18:27:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0eebffb67f772af593b242a849c92b3520c2939c8318c1d5030612ae8328c1`  
		Last Modified: Tue, 02 Dec 2025 18:27:35 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacdee43a1de0f433cb94e72b057f716650ce34102645d445a5d6194ee68d1dc`  
		Last Modified: Tue, 02 Dec 2025 18:27:35 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29b2c8d095936937be6c9ceac0e14216c2e60d4aadf3f86f05973aa5effa5d5`  
		Last Modified: Tue, 02 Dec 2025 18:27:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.2` - unknown; unknown

```console
$ docker pull kibana@sha256:691ec5ed48032217f83949140fc56a7a83e20819da0d73a7628eff6bbc51d588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5801344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9a3735c75ea3f4ea0c405475874c4602b1c45c98d66f35130b78442515fafc`

```dockerfile
```

-	Layers:
	-	`sha256:c4b798a2d2c25da952e3940666f8634dcdfd2294a1c3720d3746ccaedeed475a`  
		Last Modified: Tue, 02 Dec 2025 21:11:43 GMT  
		Size: 5.8 MB (5758118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277fcddb460ef5e496436b48f426b3d5f0fc1d06e9192fecaf41785f74395bc8`  
		Last Modified: Tue, 02 Dec 2025 21:11:44 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:45d119a7bb4c498caadb474d9b59ad9621eb16304368141d77948c97bbae13e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.0 MB (455975279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03700e0e3e2203d93e3f25dbeee603adfc4ab1188db5b76b574890efa57ae12d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 18:18:51 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Dec 2025 18:18:51 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Dec 2025 18:25:53 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Dec 2025 18:25:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Dec 2025 18:25:54 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Dec 2025 18:25:54 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Dec 2025 18:25:54 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Dec 2025 18:25:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Dec 2025 18:25:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 18:25:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 18:25:54 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Dec 2025 18:25:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 18:25:55 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Dec 2025 18:25:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Dec 2025 18:25:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Dec 2025 18:25:56 GMT
LABEL org.label-schema.build-date=2025-11-27T09:37:18.054Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c0340ed35c591c77a90ebf1c790c20aa07571672 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.2 org.opencontainers.image.created=2025-11-27T09:37:18.054Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c0340ed35c591c77a90ebf1c790c20aa07571672 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.2
# Tue, 02 Dec 2025 18:25:56 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Dec 2025 18:25:56 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Dec 2025 18:25:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Dec 2025 18:25:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Dec 2025 18:25:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a8e6716d41797344a58d1d52f4a706ac74e70c67c35f3a7161ed16cb2ba176`  
		Last Modified: Tue, 02 Dec 2025 18:27:29 GMT  
		Size: 19.5 MB (19494746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b3b636bb32dfd807b25b6174966c7d31f1afeac04c55741f74341e30286027`  
		Last Modified: Tue, 02 Dec 2025 18:27:10 GMT  
		Size: 381.7 MB (381701959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f1fe4b866ee1444c12250481a0fd90ffb5735c37df85e44b522215c13cb153`  
		Last Modified: Tue, 02 Dec 2025 18:27:18 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29379265ebdd7cf52e3855be4e2f1dbaf95cceee0cc97aec43c79d8db06a74aa`  
		Last Modified: Tue, 02 Dec 2025 18:27:20 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2ad9ce2701c6874cd4f59ebc1074d1f3b304e110074ba188bde7f5c2126a3a`  
		Last Modified: Tue, 02 Dec 2025 18:27:18 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e66bbb26ea52c192a7d8d196c723ee1970f075ac25e4bb4cdcbceb710be3cc`  
		Last Modified: Tue, 02 Dec 2025 18:27:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb35501529b755e6c5f85821962ffd8707ce302c524c6bb4bee0d060f42b3ee5`  
		Last Modified: Tue, 02 Dec 2025 18:27:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2aa3d5ee1e3dda2415fd76104a75cc5bb966f08b8764dfed2c24b43b1b303f`  
		Last Modified: Tue, 02 Dec 2025 18:27:19 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea9117aa55631a098f5cac1f4ee35deac95be8bca643ca4a20c6aa101d1e67`  
		Last Modified: Tue, 02 Dec 2025 18:27:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd0e3d05d57c0fdf496a053f4300465ec7c9ba71afc31c43cd01bf9af2d7250`  
		Last Modified: Tue, 02 Dec 2025 18:27:20 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1911b21044bac1125b829d71acca9f6b0807cfd5e73514f6490410cdd18018`  
		Last Modified: Tue, 02 Dec 2025 18:27:20 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66eeb4081496e1631a652a9c4bc3a4f3d2591e8812c5d663b3ee038b4925555b`  
		Last Modified: Tue, 02 Dec 2025 18:27:19 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.2` - unknown; unknown

```console
$ docker pull kibana@sha256:c329ba8a8b9bb62e0191a05935ccce8056033625d8a613127ea4ccb90ee791d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5068333455f0dd3b6dae247a0f7948303f499b1f646ce627baeb30f67a6e70c5`

```dockerfile
```

-	Layers:
	-	`sha256:eb529c2dd2fb8b19426b9eed8c248512ad30dd6a1c7e1d4faa21d19cbc0e1ba2`  
		Last Modified: Tue, 02 Dec 2025 21:11:51 GMT  
		Size: 5.8 MB (5756794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee2ce4d4d21dd270943812c5c9bfb35f78f34d520fbb76fd25743338ab0d619`  
		Last Modified: Tue, 02 Dec 2025 21:11:52 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
