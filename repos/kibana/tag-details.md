<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.7`](#kibana8197)
-	[`kibana:9.1.7`](#kibana917)
-	[`kibana:9.2.1`](#kibana921)

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

## `kibana:8.19.7`

```console
$ docker pull kibana@sha256:1d28569d88f6e52e1bfc7f34923f3d24749ae7de6337914ac2dd434f54ec465c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.7` - linux; amd64

```console
$ docker pull kibana@sha256:71dc9196d39832f10a65be18fe65882c59c399e53c4e303944f163b35599243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436690788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238bcd211df399d4ce21b1ef586d31db92c37e1b0782252ad75263e8d713f8ae`
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
# Thu, 13 Nov 2025 23:28:39 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:28:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:37:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:37:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:37:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:37:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:37:28 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:37:29 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:37:29 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:37:29 GMT
LABEL org.label-schema.build-date=2025-11-07T13:25:36.883Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28cf679904329ed50de370ff1e1e71f1b57996a1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:25:36.883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28cf679904329ed50de370ff1e1e71f1b57996a1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:37:29 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:37:29 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:37:29 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e831024f1e65cae7c7e27d092da8d03c06d50b739ca11159f3e8d53b4859e3`  
		Last Modified: Thu, 13 Nov 2025 23:38:38 GMT  
		Size: 9.4 MB (9432118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413e3835eb47da03dc335b427679a5c0c4ac7c4656f3a91694507c960744d84a`  
		Last Modified: Fri, 14 Nov 2025 03:18:20 GMT  
		Size: 380.9 MB (380890274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1312679a3caa1156b3e798453d802d7b24c4dc935ec9a998ff6f9664a917832a`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330ec6fad6c2c37195404b82de22ff39497e7759a6be8cefec847cdca64468da`  
		Last Modified: Thu, 13 Nov 2025 23:38:39 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2c3d951f7e8cff27cfba26fe0b8cf04cc224d8165877d5202b39fbee6953e0`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f2824797228c74ecd81482051326b7dcb654e99a76bb0d63f1a1a6cbeac0ff`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c88815a00e2ee1fbdc6a344b7f496d4886e853d319083fab0ebb4b1fde8671`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839bc2d33d02584c921fe20bb12f648b40663c8a8290077672f6b1e9aeaf4ebf`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f079f359d83263e052fe364dcf95b7000e4bed8da87df76342546dd1c924ea6`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6be2768226b4808616941db3689c7752b7939ba5056bb35a28fc4d12c80d587`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab46a087591e71b2147800a57a15b9fc197c31e3267c6051641233dc4c594ca`  
		Last Modified: Thu, 13 Nov 2025 23:38:37 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.7` - unknown; unknown

```console
$ docker pull kibana@sha256:7e4b03456994b8e86c5530d2b35a04320c07d31127a3c67d20f5d38a7077d616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba23ab72257b4d15ce49bed40726ef9551fe615ca7412146c30b6d6dde57a52a`

```dockerfile
```

-	Layers:
	-	`sha256:9f0671a2e66ed26d9b3ebe2645efd504c35f7c53db5f7ee25da6724c24412359`  
		Last Modified: Fri, 14 Nov 2025 03:12:04 GMT  
		Size: 4.9 MB (4874334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf72418f2f67a4f3983bb9e82c59bc4d65a1f05457bdc1d69c2064cd0f812baa`  
		Last Modified: Fri, 14 Nov 2025 03:12:04 GMT  
		Size: 40.9 KB (40907 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8b82f41480e00f701b5765508bf37f05acb180813f6a84289bff0e8e0fc7fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448862487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07a11b798b164f4d7112d6c0ddab89b520339bab4f687ef0ede47e13e17447e6`
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
# Thu, 13 Nov 2025 23:27:58 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Nov 2025 23:27:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:35:02 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Nov 2025 23:35:03 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:35:03 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:35:03 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Nov 2025 23:35:03 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:35:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Nov 2025 23:35:05 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Nov 2025 23:35:05 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Nov 2025 23:35:05 GMT
LABEL org.label-schema.build-date=2025-11-07T13:25:36.883Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28cf679904329ed50de370ff1e1e71f1b57996a1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:25:36.883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28cf679904329ed50de370ff1e1e71f1b57996a1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Thu, 13 Nov 2025 23:35:05 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Nov 2025 23:35:05 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Nov 2025 23:35:05 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555b2904321a495d59cc123c17789cb19eb74703f4b76d3a7bbaedefa824c49e`  
		Last Modified: Thu, 13 Nov 2025 23:36:33 GMT  
		Size: 9.4 MB (9446146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f046b6e1f3967f5bd455e37809db07978c1515ed557e31616a7e0de691f23b4`  
		Last Modified: Fri, 14 Nov 2025 03:17:55 GMT  
		Size: 393.9 MB (393914557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7743957bbd66fe2732fd3cc420ff68b980ba95a3f93dbbb428f9fd585348bd40`  
		Last Modified: Thu, 13 Nov 2025 23:36:31 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f6a0f68663a88b3f6a8b77ab28c22040b6456013381c38c977f23be8fa44dc`  
		Last Modified: Thu, 13 Nov 2025 23:36:34 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a810635ed59548280e58ba9230f96a13ab95575aeeafec71206d4fb6ee0dfa`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c891093adb2e87e5ea14ca4e1de2766d3f4973e3d210d76924720671b6bec1a1`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400782be555936668c0c0d4abf99eb77523b9104780675655801ec3b2b86e7c1`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd3462599017d3feb67ba7a48e6bef09ea15fdb478dcb6bba9848a9fa63fc6`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9885633034580c4b3cef2c775ce1c6f4ae1569c01145cb41d804dd608788c5ec`  
		Last Modified: Thu, 13 Nov 2025 23:36:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a8f163694eb13a45e458a441f62fad091ec28046c6580f05a5f9927ce434ff`  
		Last Modified: Thu, 13 Nov 2025 23:36:33 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9af3d90a714fb96f4049a49476b0ee80051cd389bd4cf5b3250292f49c2fd74`  
		Last Modified: Thu, 13 Nov 2025 23:36:33 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.7` - unknown; unknown

```console
$ docker pull kibana@sha256:1bfbbde40adb84f925f2a64ee0154d865384305a54fe9568e4bb3e57b17d3448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4916553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a57422385740c1f9073578caa9727ccec1a90fd2fdc83bda6eebee6d58b142`

```dockerfile
```

-	Layers:
	-	`sha256:90233e5142c3a2ed9ea323b7260be37235810e33a9cc02000d927f1c65fc0e1c`  
		Last Modified: Fri, 14 Nov 2025 03:12:10 GMT  
		Size: 4.9 MB (4875398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e1ae6380c0dbe8a2687d4e96f00ddd8d2c30fae2b2e466d49c7d3aa45ace277`  
		Last Modified: Fri, 14 Nov 2025 03:12:11 GMT  
		Size: 41.2 KB (41155 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.7`

```console
$ docker pull kibana@sha256:94bf78583db793ccda875f0a6cd0dcde44e4db0cc9b7137123dc5e2224a35f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.7` - linux; amd64

```console
$ docker pull kibana@sha256:44cb03b4344caeeac4bd9a809ff5acb37a5945631c77c0eee4f0455cda63b055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (437969645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a50570da5bb3c098bad7132f93a1216ccac41c7250d236ce66cbb0f69aef1ac`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:07:23 GMT
ENV container oci
# Wed, 12 Nov 2025 14:07:24 GMT
COPY dir:fd8f02dabe7ae9790ce0638d1f9e9f60d460b3580843d39cb4dee8e471c106cc in /      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:07:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:07:06Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:13:48 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 14 Nov 2025 01:13:48 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:22:41 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 14 Nov 2025 01:22:42 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 14 Nov 2025 01:22:42 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 14 Nov 2025 01:22:42 GMT
RUN fc-cache -v # buildkit
# Fri, 14 Nov 2025 01:22:42 GMT
WORKDIR /usr/share/kibana
# Fri, 14 Nov 2025 01:22:42 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 14 Nov 2025 01:22:42 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 14 Nov 2025 01:22:42 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:22:42 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 14 Nov 2025 01:22:42 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:22:43 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 14 Nov 2025 01:22:44 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 14 Nov 2025 01:22:44 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 14 Nov 2025 01:22:44 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Fri, 14 Nov 2025 01:22:44 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 14 Nov 2025 01:22:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 14 Nov 2025 01:22:44 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 14 Nov 2025 01:22:44 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 14 Nov 2025 01:22:44 GMT
USER 1000
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ccaf33a8a5b988cc6438ef064e29fd12a2f2e1feca03b5ba6dd798bda2accc`  
		Last Modified: Fri, 14 Nov 2025 01:23:55 GMT  
		Size: 19.5 MB (19536490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fcca200dfd5d7119aae2dfb72cd39822376c3516929679d5bd044e2a016eb5`  
		Last Modified: Fri, 14 Nov 2025 03:19:27 GMT  
		Size: 361.8 MB (361826516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cd92094971e6513e8f3867408a99969290fceebc5c770e813001ad083e37fc`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629c2a60b65ed81012d7232b57046897dd2539ccb6db9b663d7d07646b409691`  
		Last Modified: Fri, 14 Nov 2025 01:23:54 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85cef5672cec2586ee54e2c405c2d86a57c02528441c62cb7dddcd31af9b51e`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f967a7cbe2d36b511d03f61552481180c09af5bc0192389363774c51d11b2f`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a40e13d492269deba483c14c33b62b6aed8442f7f0eee95c438002c18bb63b`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f67408200f08411a4a34d30f19ed0802daa580583d258abaf1f33c00fd89125`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 4.7 KB (4740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baf315fb9f690943b0aec6911d62915f63e513048bfc5cf214f33198c4273a9`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8983a6c78790dfd37ed376faa6215f016e28d924c4f92b00792fdb6cfef8db0f`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087deab555f84408e7926f6cb25dd35c8ae4b0193638d12f970461fd4011dbf2`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b072aedd5a2aa657b711b3a8501bcf78b11f847277900778bc7f253688186eaa`  
		Last Modified: Fri, 14 Nov 2025 01:23:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:fee4896320869fa426a8d8b4b1d72f22be886ebe41ef4d1f626b6a64a6f179f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4623278ef97309f47eef9d3e92a7323f7672c6d5e8bdcff48a04540a04478e`

```dockerfile
```

-	Layers:
	-	`sha256:d970d99278ff46d47a9a1355dbd5985e3512f323a5be545c7d1aa252f9e39f06`  
		Last Modified: Fri, 14 Nov 2025 03:12:13 GMT  
		Size: 5.7 MB (5655525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abcbbb8386000a06ca0ebbed1655e14a42d836bb567319ea3887ef83bec2bbc7`  
		Last Modified: Fri, 14 Nov 2025 03:12:14 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5c6c6b316e7e404604dd4ed54340204662734316efc398c4a2521102745637fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449118551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938e94eb2f29b031a35ba727a540a76027074e78b91df4a468f605ddf4ed625d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:10:11 GMT
ENV container oci
# Wed, 12 Nov 2025 14:10:11 GMT
COPY dir:306690a4b33e0c2c47cf50b466ed471eb7ab206a490a8f74fd060934dfe49241 in /      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:10:12 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:09:54Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:30:00 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 14 Nov 2025 01:30:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:37:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
RUN fc-cache -v # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
WORKDIR /usr/share/kibana
# Fri, 14 Nov 2025 01:37:11 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 14 Nov 2025 01:37:11 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:37:11 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:37:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 14 Nov 2025 01:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 14 Nov 2025 01:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 14 Nov 2025 01:37:13 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Fri, 14 Nov 2025 01:37:13 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 14 Nov 2025 01:37:13 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 14 Nov 2025 01:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 14 Nov 2025 01:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 14 Nov 2025 01:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695d9740824113abe669e4badb8129449f3568c949396bbb87fb1a99e9b5cc8b`  
		Last Modified: Fri, 14 Nov 2025 01:38:35 GMT  
		Size: 19.5 MB (19496398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c626333cd7b1e939c59dcf478abb57e48ddd55f5e3ed9e618671abcc2a578`  
		Last Modified: Fri, 14 Nov 2025 03:19:16 GMT  
		Size: 374.8 MB (374844393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b152fddf947ab5b4ced379981febae1607bc2539b9aa5cba90a1984e7d5e62`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea155ac95654146fb3e131a0cd7579648dd93cba641835759d59d0bff2d3bbfb`  
		Last Modified: Fri, 14 Nov 2025 01:38:34 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f5557aca6fd8567a295b11db8e8a6ed5f6e60c395b9477f9af169afe127fc9`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b5b2285104869688e6c77216e59ee4300b6f8426d729fab32a62fbeb0bf2f1`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcdef3743b2824472cf9d0c4f4f827756556c8c2e1cb918c3fe25e219797b72`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12950753a9e85638f63b1ec4a305a058949c0a4423cbffa7452d864503b12fd2`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 4.7 KB (4742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6d86009e26a6655ded8b3c5d9ddd5e5f4774d29fb8c0b87b064808042d1098`  
		Last Modified: Fri, 14 Nov 2025 01:38:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b607d60d6dc9bb5272d476e27ae0cb8416522c13787b210abf5bcf1c9a9d2d4`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8127114d9ccbbe89ca7f7c653f18104a76664f481cb09fa204fc01628085f9`  
		Last Modified: Fri, 14 Nov 2025 01:38:34 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76016c587a3f975edfdb3840c9e5714f18744819ec46a5ca8a6ff2eaccc48356`  
		Last Modified: Fri, 14 Nov 2025 01:38:34 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:dfc96b6d9088e8d45cf587893dc011a5e190462330f797e4410a2f880ebab274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5697683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa61026d89a53b5c4aea15d5a4248a8cf88a8cb866f2e36ba179ad07e1f4f74`

```dockerfile
```

-	Layers:
	-	`sha256:c1788c206c67a587ae467297126822a7b0b0ae5317189d352cadbfc58be338c3`  
		Last Modified: Fri, 14 Nov 2025 03:12:19 GMT  
		Size: 5.7 MB (5654201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4b5828adf793413b0374f9a96b8cfd4b4a5d15749b1ac921390e386781a093`  
		Last Modified: Fri, 14 Nov 2025 03:12:20 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.1`

```console
$ docker pull kibana@sha256:45db474aca9b33d347da9ac490cd9933f54fa1552046589d4941081b236b2334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.1` - linux; amd64

```console
$ docker pull kibana@sha256:9bb2fa43ce6a31cac2a9adc1bb557c747451300081daeb1370709fde544d4433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.3 MB (436340122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cb94f2c6ea4c9ff92e79206ba40267eaa71e8a563c05880f4966c84e06a162`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:07:23 GMT
ENV container oci
# Wed, 12 Nov 2025 14:07:24 GMT
COPY dir:fd8f02dabe7ae9790ce0638d1f9e9f60d460b3580843d39cb4dee8e471c106cc in /      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:07:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:07:06Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:14:15 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 14 Nov 2025 01:14:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:22:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 14 Nov 2025 01:22:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 14 Nov 2025 01:22:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 14 Nov 2025 01:22:55 GMT
RUN fc-cache -v # buildkit
# Fri, 14 Nov 2025 01:22:55 GMT
WORKDIR /usr/share/kibana
# Fri, 14 Nov 2025 01:22:55 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 14 Nov 2025 01:22:55 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 14 Nov 2025 01:22:55 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:22:55 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 14 Nov 2025 01:22:55 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:22:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 14 Nov 2025 01:22:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 14 Nov 2025 01:22:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 14 Nov 2025 01:22:57 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Fri, 14 Nov 2025 01:22:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 14 Nov 2025 01:22:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 14 Nov 2025 01:22:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 14 Nov 2025 01:22:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 14 Nov 2025 01:22:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f8e8094f850cfe31a0b6c149d20c3d0677c2b67d433910b3c8386b0e0b87d5`  
		Last Modified: Fri, 14 Nov 2025 01:24:11 GMT  
		Size: 19.5 MB (19536498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56202bf61f7c81817402c1e3024e95d90664d055b25b565481685494e5c702c2`  
		Last Modified: Fri, 14 Nov 2025 03:12:53 GMT  
		Size: 360.2 MB (360196844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ce827b1e04c8ff13296386c16995cb2f6a7a7d1d59d1c098cd957cf18ce033`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b354d682119e8cf81ecb05fe6ba63516842aa5fdd3f7d69352ce423b4d48b55`  
		Last Modified: Fri, 14 Nov 2025 01:24:11 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c922130e6e7a696df3df447f4f60be8df91c23d848636bf4d7ab56a6f8aec`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7d54f955a5deb643cdb02fcbf0ef583036f61eeb10c45014f4cbf21740acbc`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a29489223db53661417c1f7bb1a8ce859eddfb8f70f61d7ae5bfbda5ab919`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faf1bbf32f2d36783ceb64e3cd3418028acb2237166e7b3a5c8608a9476c1ee`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 4.9 KB (4891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8726e747bd0c940e2b2f38d00b227cc4f1786d59b26600af67b1ee3b33f7ec`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668f2227e297fe424c8921e0a86dde59fdc397c09b61fd535bdd1654ea2744bd`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569fae411db7ce35c46a53014565d44d7e1ee9beecc0d5ceaa350d887194313`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bc3d003449a7febe5c8e4ce33cc390c33b3e1e3efcebad4b1b9415f73f5061`  
		Last Modified: Fri, 14 Nov 2025 01:24:10 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:bf374d3ac8fab0b16ebbd4a899db697517491cfc306de6f64b332d4b8f04dea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d39b2eb0bfd1d51b9e839981fbfbdcf32632f8ec4d12342077a2f791090fbf5`

```dockerfile
```

-	Layers:
	-	`sha256:718a8f41f28e1746e689302716434081bd1ab01d9eb434ee02173ee3064eee6d`  
		Last Modified: Fri, 14 Nov 2025 03:12:25 GMT  
		Size: 5.7 MB (5713248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54e7c17d985c02aecb0d9dde1b39c1270c29006022e58dd43575c0fa960873`  
		Last Modified: Fri, 14 Nov 2025 03:12:26 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3faaa4e6b8e6f888a4a1d755b9b34799c956ddbf5f30b22f520fd66945211bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447504148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392896585934551a495aadee805c2496fd2efc232065cf4ff05157fe309a87bf`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:10:11 GMT
ENV container oci
# Wed, 12 Nov 2025 14:10:11 GMT
COPY dir:306690a4b33e0c2c47cf50b466ed471eb7ab206a490a8f74fd060934dfe49241 in /      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:10:12 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:09:54Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:29:51 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 14 Nov 2025 01:29:51 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 14 Nov 2025 01:37:11 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 14 Nov 2025 01:37:12 GMT
RUN fc-cache -v # buildkit
# Fri, 14 Nov 2025 01:37:12 GMT
WORKDIR /usr/share/kibana
# Fri, 14 Nov 2025 01:37:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 14 Nov 2025 01:37:12 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 14 Nov 2025 01:37:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:37:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 14 Nov 2025 01:37:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 14 Nov 2025 01:37:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 14 Nov 2025 01:37:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 14 Nov 2025 01:37:14 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Fri, 14 Nov 2025 01:37:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 14 Nov 2025 01:37:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 14 Nov 2025 01:37:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 14 Nov 2025 01:37:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 14 Nov 2025 01:37:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba18c5461699a4f039546a252cd0ee7d92e0b4e4a3a198595a6c28c592f66ae8`  
		Last Modified: Fri, 14 Nov 2025 01:38:35 GMT  
		Size: 19.5 MB (19496416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a837bee9fe28487b5c78ff4045682e5bb9799113419fd164f7c1450ee483236a`  
		Last Modified: Fri, 14 Nov 2025 03:20:26 GMT  
		Size: 373.2 MB (373229835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74c2385bc7ff4000cd7075a00a7320acbf47f431247fae4172f82e0c1501178`  
		Last Modified: Fri, 14 Nov 2025 01:38:32 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1651e7953a79741f890d810f4497dbf4cf6df5adb9fbb7599a7905adcf1331`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2542349847a82c9c160b4abb6e29627f63eb2501ac9eaaef582f9c63902e793`  
		Last Modified: Fri, 14 Nov 2025 01:38:32 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1791e51cfd5197a40410f2071c58836378fa9114772ae39893f675c8d0361aa2`  
		Last Modified: Fri, 14 Nov 2025 01:38:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9781afa6e11c1afb2d4d03f509e305b88b8a29c1dbd7876ae5abded4e082afa`  
		Last Modified: Fri, 14 Nov 2025 01:38:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e603480771edef7f2bff469cb03dbdd77d6be219ef56febf36e339f4582ce176`  
		Last Modified: Fri, 14 Nov 2025 01:38:32 GMT  
		Size: 4.9 KB (4892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8288b045c8ce463ad7f2c9a5451b9a70717bc83e1998ba3e0a547ccb2152c87`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b607d60d6dc9bb5272d476e27ae0cb8416522c13787b210abf5bcf1c9a9d2d4`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0f64d053fc17fcae81ede6fe2ec560025be3c659bd0b590d072bdaf7ffe18`  
		Last Modified: Fri, 14 Nov 2025 01:38:33 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3da05ab4e108352bcd14155d2f3f25ffb67c8836caaaedfd71063e4e555345`  
		Last Modified: Fri, 14 Nov 2025 01:38:32 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:79a1c82ae379b61adb2e6df238784bb784b1712471032398922b8f32dbbec09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03398d6c4627eed6d42054d3c5bddaf184568cf1da4c614e92e3fd385849903b`

```dockerfile
```

-	Layers:
	-	`sha256:2bb0d5ab12e48505a7bf4662787424185d095cdef311d7d89352fe15965ebf27`  
		Last Modified: Fri, 14 Nov 2025 03:12:32 GMT  
		Size: 5.7 MB (5711924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3602ab9ec8eb8e9a662f439d78082ab6cd4e0f4cd067bfed331412dc8d07f575`  
		Last Modified: Fri, 14 Nov 2025 03:12:33 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
