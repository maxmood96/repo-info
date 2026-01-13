<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.9`](#kibana8199)
-	[`kibana:9.1.9`](#kibana919)
-	[`kibana:9.2.3`](#kibana923)

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
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdb63166b01065b5f7b99b6c9aef0b064c2619c8a8d2aa28900c35620dad640`  
		Last Modified: Tue, 13 Jan 2026 02:48:22 GMT  
		Size: 9.4 MB (9432171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e243fbaf8e56d5b355b644529d3ed4788c625a92dbbbed24fdb160ca65e1a`  
		Last Modified: Tue, 13 Jan 2026 02:50:16 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49d4ff80eb1fe4f3116402fc8f8b14f01dd2667c426dd0c6ba3a71ed0a4f7ae`  
		Last Modified: Tue, 13 Jan 2026 02:50:16 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48405d79663978c1cf545837462f1c20b1c07ad7bf145101b7627051b2bc13d8`  
		Last Modified: Tue, 13 Jan 2026 02:48:23 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10aa325ed52e36638eeeb312d4f855b884465eb853383b69373091f002014281`  
		Last Modified: Tue, 13 Jan 2026 02:50:18 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e171d897aa16a8798e29bab0abcec849131cd946dc34713709b638e7c904ae`  
		Last Modified: Tue, 13 Jan 2026 11:18:46 GMT  
		Size: 298.1 MB (298112553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd272ceee08e890fbedfc09bf4dd061bbc4cdbb94d8a97ecdc2026c1ea650c5`  
		Last Modified: Tue, 13 Jan 2026 02:50:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9ab140f6e2dfdf61227617e6a235aa453a7a3f6495115ae02e6fd77406f46`  
		Last Modified: Tue, 13 Jan 2026 02:50:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5b9c0f18f07e84fb9334b4b92b4c3c56b4fd1cf8fa909b539c13b757e88328`  
		Last Modified: Tue, 13 Jan 2026 02:48:32 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de8f438b26057468d57ceec2555726a6b4dedb5198d5a72fc8c9ecd062a05e7`  
		Last Modified: Tue, 13 Jan 2026 02:50:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1b7f1c0d124847f7c8bd31f3a70c1960fffbc81978dca5f157529e7ae128a8`  
		Last Modified: Tue, 13 Jan 2026 02:50:16 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718e8bc690f6e59d6eed6bf905a7b0b1f518eea1b038ab980ac727f64a813b6`  
		Last Modified: Tue, 13 Jan 2026 02:50:13 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:43:10 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57fbad5574700428d9e57e578aa8dce94626a1457e6016765d503452d6e2e899`  
		Last Modified: Tue, 13 Jan 2026 06:43:09 GMT  
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
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6397d3511035aaa5996ddbd63c844242cdf265782c4d0652b67548aa3fef509a`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 9.4 MB (9446173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1853a381f41232f921e5526c3e6700154b827f6949ce80249b881bc6d699cd09`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a760837544bebe14a33bb967a1935d4a4d15c3abb9227281080d71dbe975e53`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922bd60bd5fec7692b52505f3a4906334bcbb68e40c63f2ec9e47f2af918012`  
		Last Modified: Thu, 13 Nov 2025 23:31:36 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89931a8edb2c8dbee44c71f14803f8136f4ec18de1703d9337b4641620485f85`  
		Last Modified: Thu, 13 Nov 2025 23:31:36 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf67254e8331c96e4c2f96142859368e57085c91814b2f0e300934367be2c05`  
		Last Modified: Thu, 13 Nov 2025 23:31:44 GMT  
		Size: 311.1 MB (311148121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55926e73b726f9b587823eac64e2486adf2c4bc7eaaf0dc86a1823587916f465`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f1fee166071308bd9f88d3a9c288789bb822f58d513126237e97547bfffb71`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12355655218fe6c3b48187926fe316193619b4b7b9eae9eab2d102d577d00a30`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a729783706fcbd9ef444378dee2624e0fffa33a4213baa8a774ff08d00b3d2`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3565fad2095d35954b8261412110b44af400bcd11be235b398ae7faf5599bc`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54760310f932ac7c65ec67da5c9eb6f576c221ed4872eb417a199ea2a76978`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
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
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.5 MB (3507898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee98450ea19b52544a490c084455349bf886d683fc7244bef3585fb42d8c9cf`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
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
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaa7e3f5276d9a52d6abe8527fe00e8cb71ba993e041bcd1c37db82c8565f62`  
		Last Modified: Tue, 13 Jan 2026 03:05:34 GMT  
		Size: 9.4 MB (9432182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babb566056a2f72f3c0d36be7a38997b8d1d6462fa0ec8fcd234041db225389c`  
		Last Modified: Tue, 13 Jan 2026 07:05:07 GMT  
		Size: 368.3 MB (368279132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddec7aebe1d1a4de4d26a7d08e1a2884cddaaad30f12908c9f66aea29148e344`  
		Last Modified: Tue, 13 Jan 2026 03:05:32 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14ea6f6f4524247905656484936f3bba1a49c33d1360378e554c90512d922df`  
		Last Modified: Tue, 13 Jan 2026 03:05:35 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a1887c4ab1d067a93261b962ac9fc4ee3820741c138017f89775ba504c0c4a`  
		Last Modified: Tue, 13 Jan 2026 03:05:34 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be88165050c540019b55dcb3913d33e928cdee0c4950798c1cf7d4f067d6d7e`  
		Last Modified: Tue, 13 Jan 2026 03:05:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47beb95e0935f6cd8b92bf84d7fcb59013455e99af72163cce89e37f559ef66`  
		Last Modified: Tue, 13 Jan 2026 03:05:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e29c2f534b0713ae1eec9e185d5ffecdf40705e8627f6ca30fc1ccaab92ca3`  
		Last Modified: Tue, 13 Jan 2026 03:05:36 GMT  
		Size: 4.8 KB (4768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3768e40446a0706b1d9c9f95a34b73f1b6453918f88b905d5799df0d5c600ac9`  
		Last Modified: Tue, 13 Jan 2026 03:05:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d1815f836fc48b66044cc1656e343143eb66fbe43e74d8dc8d4f7908b2233f`  
		Last Modified: Tue, 13 Jan 2026 03:05:37 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf42b8285681325cd51e1d6daff0127a6c5590674382b14d5242e9a185648b8f`  
		Last Modified: Tue, 13 Jan 2026 03:05:38 GMT  
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
		Last Modified: Thu, 13 Nov 2025 23:37:52 GMT  
		Size: 4.9 MB (4856890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30130bbfba23015d367d7aeab62a8d79e080423b3f708b6eaad4cfa1d184bd66`  
		Last Modified: Thu, 13 Nov 2025 23:37:51 GMT  
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
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de63df616becf613cf5fe961e187fc6129aa4b6d1b5509db6b1df0c8855a7a7`  
		Last Modified: Tue, 13 Jan 2026 12:17:13 GMT  
		Size: 9.4 MB (9446139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c090a108fe140a15dedec5955270529bff007c1f1c9a79677aa83379c3f4b780`  
		Last Modified: Tue, 13 Jan 2026 12:17:55 GMT  
		Size: 381.4 MB (381407353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7addf77df7fe3204f04de322cf7ea86b59e69c8aa9e26fd50a7d9029226be5`  
		Last Modified: Tue, 13 Jan 2026 12:17:12 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a65f8bbd7e9d95181ae79ffd18b90a44d166c7025a2325e93eb0488cce6d6c`  
		Last Modified: Tue, 13 Jan 2026 12:17:15 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8eb30e0d24f5bd8f1e55fa2c70d40abeb3433cf53b0fd561aaf5070fe43193`  
		Last Modified: Tue, 13 Jan 2026 12:17:12 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410b06427c0b5cd07cc2eea851aa0bc7da593c1a21c9c9d673677c9867b1bca5`  
		Last Modified: Tue, 13 Jan 2026 12:17:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cfd7eb4342b3ebb07a436bc7eabb448cfb63b08af09ff8a2a17f506f43da25`  
		Last Modified: Tue, 13 Jan 2026 12:17:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7486155002a8e617ffd5b2f54347df258b3acb32f2c6530e0781d42c4fae35`  
		Last Modified: Tue, 13 Jan 2026 12:17:09 GMT  
		Size: 4.8 KB (4764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bba29ab01d8b73367d63e6ad72b76b69fc579d73b09a2b157e9c559c2a4389`  
		Last Modified: Tue, 13 Jan 2026 12:17:10 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e8d5b05c91bf573a0a0ab1ff3ac21ec59e16c1c610d4f760e59c7ae083801`  
		Last Modified: Tue, 13 Jan 2026 12:17:08 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87df0fbd969ca87b03ee7923e2deb35235ebdf8c4094c4ebc4df8817e742d069`  
		Last Modified: Tue, 13 Jan 2026 12:17:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 12:17:17 GMT  
		Size: 4.9 MB (4857954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1dcf166553967c58eae09a06b1350bc953ba549467c61d69fd22deca57c029`  
		Last Modified: Tue, 13 Jan 2026 12:17:07 GMT  
		Size: 40.9 KB (40930 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.9`

```console
$ docker pull kibana@sha256:26e72b6d615180b091a1ed15068dd1a352fcff84c64f093708ece50e939ecf7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.9` - linux; amd64

```console
$ docker pull kibana@sha256:93a1079a9a9ed40d1aae740b83aa9305fb3f8d95875645ac5a4a3fe28c64d705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440609194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24770ff1a14b6936bbde70bc42cd5278f99318ae033b0411234ef66300b382f`
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
# Thu, 18 Dec 2025 19:12:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Dec 2025 19:12:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 19:21:21 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Dec 2025 19:21:21 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:21:21 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Dec 2025 19:21:22 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Dec 2025 19:21:22 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Dec 2025 19:21:22 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Dec 2025 19:21:22 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:21:22 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:21:22 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Dec 2025 19:21:22 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:21:22 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Dec 2025 19:21:23 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Dec 2025 19:21:23 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Dec 2025 19:21:23 GMT
LABEL org.label-schema.build-date=2025-12-16T21:11:28.340Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=42f1c10f1e8aa480aaf63cdd403d2f3a3eb42cd3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.9 org.opencontainers.image.created=2025-12-16T21:11:28.340Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=42f1c10f1e8aa480aaf63cdd403d2f3a3eb42cd3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.9
# Thu, 18 Dec 2025 19:21:23 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Dec 2025 19:21:23 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Dec 2025 19:21:23 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4659de0c0c8f19cf97b9c2e450f1b726d44d6d63dd0c60349b1634ca94612ed`  
		Last Modified: Thu, 18 Dec 2025 19:22:35 GMT  
		Size: 9.4 MB (9432486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da18d10a26c798073cb4e965c31af767b73c6295e9a4a895b31df24c23f3b1e`  
		Last Modified: Thu, 18 Dec 2025 19:23:49 GMT  
		Size: 384.8 MB (384808294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c007882f6e9a36dad60fb473c8554e032e182911a9dd5fc0f05ebec85a1c7c2`  
		Last Modified: Thu, 18 Dec 2025 19:22:34 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d75350af1322e19e5febf289a68b2b1e5b6187409a9b7e7128c660ff70060`  
		Last Modified: Thu, 18 Dec 2025 19:22:35 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581a4d8824e6cd8e356d2ec5de0496e48e3d2c9e2d003bc99396fce8f077ca8`  
		Last Modified: Thu, 18 Dec 2025 19:22:37 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef632444f63051dac94c20816937980e16574b02998ebb39e63e2aa5ddb866b5`  
		Last Modified: Thu, 18 Dec 2025 19:22:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a67c7bf44030a252f2e693e57e5e921cea160654b5d1e50f84fc0eca2ba87`  
		Last Modified: Thu, 18 Dec 2025 19:22:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff376f168ef1b054fcab6f574ac7b6a0c36a5091cf8f1b6c96028600bb0b4a3c`  
		Last Modified: Thu, 18 Dec 2025 19:22:34 GMT  
		Size: 4.8 KB (4822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab449cbd68a9a28870a24b06be9d0f51b15b9af6178c4c39267339ca024c57`  
		Last Modified: Thu, 18 Dec 2025 19:22:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf37b3337ec91ff0132c298a876e006505217a9e36cf02fcda51b36f2fbe3ae6`  
		Last Modified: Thu, 18 Dec 2025 19:22:34 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa723d2489aece9550a80f65178dc54d380c99f54b9a064fe03d8be4910a01f`  
		Last Modified: Thu, 18 Dec 2025 19:22:34 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.9` - unknown; unknown

```console
$ docker pull kibana@sha256:a66c6c7b0fde8ef63e43f99d219ccbf2707b53daaccb55a4939540a24c1788f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4957549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f28af98d87d457a4e45e970b80cb88345e8063898dcd2b1ee6fc4ee02452d5`

```dockerfile
```

-	Layers:
	-	`sha256:124f2c5c54d23919b55dfcd94f95cc9a2367808bd0e82269c79f7d63985309fd`  
		Last Modified: Thu, 18 Dec 2025 21:11:49 GMT  
		Size: 4.9 MB (4916642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d124d9857e061b7d35e6ad082d6d8365f7f5c086000d0c3584dea4e01d8320a`  
		Last Modified: Thu, 18 Dec 2025 21:11:50 GMT  
		Size: 40.9 KB (40907 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.9` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:be6a485c1a88c77bf21a34218f05db09a54eb111f9d967d70ec035a5c7c97e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.5 MB (453507172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f11e9d32545ddaa2582d414973b1d60a3525cfbe2f14665924db81502c00b44`
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
# Thu, 18 Dec 2025 19:11:42 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Dec 2025 19:11:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Dec 2025 19:18:49 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Dec 2025 19:18:49 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:18:49 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Dec 2025 19:18:49 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Dec 2025 19:18:49 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Dec 2025 19:18:50 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Dec 2025 19:18:50 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:18:50 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:18:50 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Dec 2025 19:18:50 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:18:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Dec 2025 19:18:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Dec 2025 19:18:51 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Dec 2025 19:18:51 GMT
LABEL org.label-schema.build-date=2025-12-16T21:11:28.340Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=42f1c10f1e8aa480aaf63cdd403d2f3a3eb42cd3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.9 org.opencontainers.image.created=2025-12-16T21:11:28.340Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=42f1c10f1e8aa480aaf63cdd403d2f3a3eb42cd3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.9
# Thu, 18 Dec 2025 19:18:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Dec 2025 19:18:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Dec 2025 19:18:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d44a57dcc4c8051b5e158e40a7f2d1182d9afb3932f8746f85e3fd09d2bc777`  
		Last Modified: Thu, 18 Dec 2025 19:20:12 GMT  
		Size: 9.4 MB (9446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675eaf7048150408637013c181a8513e19c8352286caa870be6bf6eb011858c`  
		Last Modified: Thu, 18 Dec 2025 19:20:25 GMT  
		Size: 398.6 MB (398558665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d313e9bf0b9ff1066ea42f8f5ac051d3c89afa104c70867badb856a5d37aa381`  
		Last Modified: Thu, 18 Dec 2025 19:20:11 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef8ccecd4bb132d270d4f72d57f863332c8bb21c65d309854463977088eb23c`  
		Last Modified: Thu, 18 Dec 2025 19:20:13 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ea303a37fc7d316038184aa67a9d8ec8d20813f0c264e1a7e2aee6ee531c5a`  
		Last Modified: Thu, 18 Dec 2025 19:20:11 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118fb32f1bb674ef7f2568cbad6c559d95e5a8a109db4b9e1e911f1c4572d84a`  
		Last Modified: Thu, 18 Dec 2025 19:20:12 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02250a6f50616202cada227a9f1788ac80d0d2677b379371d6a2aaad8f851d0`  
		Last Modified: Thu, 18 Dec 2025 19:20:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e80a6fba927794aa60368e3cbdb64bedd30dae6bd44dc9c27393a5cf05257b`  
		Last Modified: Thu, 18 Dec 2025 19:20:11 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918ff28c46fef8341828520decb30dabff2aac93aea1eb50253b2c27a373f6b6`  
		Last Modified: Thu, 18 Dec 2025 19:20:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f57c7b6cb22741739660033a4ae97772504e989eafd9f48041e6d5c776a471`  
		Last Modified: Thu, 18 Dec 2025 19:20:12 GMT  
		Size: 158.0 KB (158000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8364838bc5145793dc1425446479ac8e26cfce9e13014760a6cf888af350291`  
		Last Modified: Thu, 18 Dec 2025 19:20:12 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.9` - unknown; unknown

```console
$ docker pull kibana@sha256:d99b51a6e381e60fcff09156f18283dc15b6652087a55e543750c1413ce87b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:330ffba703d4dc7fa3fd721bfee3b2f288a1d77f831f17730710f00f303c51e4`

```dockerfile
```

-	Layers:
	-	`sha256:0f53a491f13e0c8bf247ccc187920285582e356b93f3e5fffb07693a595015ad`  
		Last Modified: Thu, 18 Dec 2025 21:11:55 GMT  
		Size: 4.9 MB (4917706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12467547d93aff2dfd1a181c8bdc7c5d8b7496252c6484e2e29922ce16e7a6a1`  
		Last Modified: Thu, 18 Dec 2025 21:11:56 GMT  
		Size: 41.2 KB (41156 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.9`

```console
$ docker pull kibana@sha256:4413d2486a9c3b32f48ce9bef10072d7e899b152b65911bfec3d2f139e800d5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.9` - linux; amd64

```console
$ docker pull kibana@sha256:0a6364f52ac9aa1a4a8f69440323503650c0974cd1b3a6d14122f917a19ed650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.1 MB (441142493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c53c3060f4647ec89bf75d90a08e910da850b078587f762da886bec42238431`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 18 Dec 2025 19:12:06 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Dec 2025 19:12:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:20:51 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Dec 2025 19:20:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:20:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Dec 2025 19:20:51 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Dec 2025 19:20:51 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Dec 2025 19:20:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Dec 2025 19:20:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:20:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:20:52 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Dec 2025 19:20:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:20:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Dec 2025 19:20:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Dec 2025 19:20:53 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Dec 2025 19:20:53 GMT
LABEL org.label-schema.build-date=2025-12-16T23:08:44.328Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=126c439648663caa7554075ebc3d1e9a6f8ad93c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.9 org.opencontainers.image.created=2025-12-16T23:08:44.328Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=126c439648663caa7554075ebc3d1e9a6f8ad93c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.9
# Thu, 18 Dec 2025 19:20:53 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.9 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Dec 2025 19:20:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:20:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Dec 2025 19:20:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Dec 2025 19:20:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96d995e7efec9b1b25e26ddcc146d4f626dea3067e52d2b09af41eb8c96df2f`  
		Last Modified: Thu, 18 Dec 2025 19:22:08 GMT  
		Size: 19.5 MB (19533491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dc24b288067a4aaf227e544bee38fc382ecd04d724824f2af398491e45006c`  
		Last Modified: Thu, 18 Dec 2025 19:23:25 GMT  
		Size: 365.0 MB (365010000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64644ddeaea6a1078117a77069f603c426059260e3a654fc4ab9e3fbf3abbd29`  
		Last Modified: Thu, 18 Dec 2025 19:22:03 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3a6f1f9c065740d43eb3525e0934f926c8d9a8f9f1594587bfb1029d7ed815`  
		Last Modified: Thu, 18 Dec 2025 19:22:05 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e304083b7f5fb8162dde9776fe04903a2bb33be966adf71137f3ac583b4c7`  
		Last Modified: Thu, 18 Dec 2025 19:22:08 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb1fde667ee842ae3334c8adc841d7614882363dac26dbec9bdca2dfd6f0ee7`  
		Last Modified: Thu, 18 Dec 2025 19:22:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fdb77f8d1a5128b765f5f582679e00c7982d46e51330352012abe98f6ee333`  
		Last Modified: Thu, 18 Dec 2025 19:22:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4ba1d3c098b5fe589b031de64496b829e213a84d0e3aad51d0e83d193bc19e`  
		Last Modified: Thu, 18 Dec 2025 19:22:03 GMT  
		Size: 4.7 KB (4744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b06a69047665da5c5e94f79451600b79847345e121d93c0c92c274822bd70d3`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea623ecf385bfab622753418ee967b6d8bec8bba376cabcb279fd33f30ca3eaf`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c428f9bbe0756f7f947d992350226ecb6489845f1d240fdf3fb2adbd745ce17`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773c4a1dba0a7b0cb8290facbac73b488932c896b1397827a8995321034a7807`  
		Last Modified: Thu, 18 Dec 2025 19:22:04 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.9` - unknown; unknown

```console
$ docker pull kibana@sha256:80676275b1d788c999cfcc87d2e1a9462f7b8431268d37e789b86638177b2f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5715013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e970b75852457ccecf90a4f5c2585ccf05893c157746a9cf2275d271c3da8`

```dockerfile
```

-	Layers:
	-	`sha256:864a6093ada2a0ef9ad3add5c60d50a73f3fe9467619873c492a73c7308bdae3`  
		Last Modified: Thu, 18 Dec 2025 21:12:00 GMT  
		Size: 5.7 MB (5671787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3887d44d9088f51dfb1397f13c85eef7fe4f7539097b6c98b041967bd3662c`  
		Last Modified: Thu, 18 Dec 2025 21:12:01 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.9` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f0b1b1b693a9de4c86a0ca095be15f5e39e1bb0a04d5fb7923d6bae6021f31e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.0 MB (453008766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf28ce322a8c4c91eafb57b6392aab5377fa5bd26c502767043203b51cbbde7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 18 Dec 2025 19:11:41 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Dec 2025 19:11:41 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:18:43 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Dec 2025 19:18:44 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:18:44 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:18:44 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Dec 2025 19:18:46 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Dec 2025 19:18:46 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Dec 2025 19:18:46 GMT
LABEL org.label-schema.build-date=2025-12-16T23:08:44.328Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=126c439648663caa7554075ebc3d1e9a6f8ad93c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.9 org.opencontainers.image.created=2025-12-16T23:08:44.328Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=126c439648663caa7554075ebc3d1e9a6f8ad93c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.9
# Thu, 18 Dec 2025 19:18:46 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.9 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Dec 2025 19:18:46 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:18:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Dec 2025 19:18:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Dec 2025 19:18:46 GMT
USER 1000
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba05ffaac2bb295a12d9f719c9b02303c0bacf0abeacf7b7725616788b4524e`  
		Last Modified: Thu, 18 Dec 2025 19:20:15 GMT  
		Size: 19.5 MB (19492912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79d001ef7a372ac7adadb082d7d803443d4a9a03e1fd8518b6642e0886773ff`  
		Last Modified: Thu, 18 Dec 2025 19:22:18 GMT  
		Size: 378.7 MB (378736306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797ad1ee48f73f56e11b7d53a3b5e4251c0f921596217f36980dc1a97f549bb5`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aa4d4f15e2d45c24ef9b4f3e29eb66d4bac9bc12e5d3bb8ba648907688e8c8`  
		Last Modified: Thu, 18 Dec 2025 19:20:07 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7956f76f7b8c730fb8454aaff529770d2b1b2551dbf9b619950baec20456486`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397128a3363672994acbd5ffc89377ec542e1a435651b90a2b9f69ff5296c717`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a393e43ec9f5115f200205ba947d653a6219493cebb61da925da0574dcfbe3e`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ee5de902230457c66bc4fbb5c7f49b7d740c9e92e1d426d47b9cd21b7b38f`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 4.7 KB (4743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc1dc2bc46a36e3b348e102bcab93b0de9f5cf3ac8cc49063e54d868cb2df16`  
		Last Modified: Thu, 18 Dec 2025 19:20:06 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12d5fc200f793b6c973b938d1cc964062009ea89533a7e19e66917331bba267`  
		Last Modified: Thu, 18 Dec 2025 19:20:06 GMT  
		Size: 73.5 KB (73454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66474c342bc9e7a0384a46c8418ea01a27d870f84fb0b0d86c8b2e952675ed1a`  
		Last Modified: Thu, 18 Dec 2025 19:20:06 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdabd875f70431fcd656d478b7c5809927731664392e87f9ed11d772a6afa086`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.9` - unknown; unknown

```console
$ docker pull kibana@sha256:f80b00291f321d66f7b6a7a3b0f56b82f203ed2714e7e5706479d164a90830d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5726ca7cef0849fa57802833d6111921da54b07e2b61e770676f28ea226e2a58`

```dockerfile
```

-	Layers:
	-	`sha256:3a31543fe16e792a5ca3583b06d2837306d7d9e107feb980330f8923bab5b834`  
		Last Modified: Thu, 18 Dec 2025 21:12:08 GMT  
		Size: 5.7 MB (5673795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc301204f1b211bb328d01430690e215c13242160d2f53c7bd635ac312d4f0a`  
		Last Modified: Thu, 18 Dec 2025 21:12:09 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.3`

```console
$ docker pull kibana@sha256:1bb55c8cb4acb0c970dddf0251114c6d85c90b1cc763c1408431355e0ef7f6d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.3` - linux; amd64

```console
$ docker pull kibana@sha256:86ad62e125f69f6061a8c7dff5fdbeb33af77ebb8d73d3c89ade158fc7582f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447213112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01211882249d866783326dbbb7a01e980e256d67a3cb86646baf4faa740384c2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 18 Dec 2025 19:12:07 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Dec 2025 19:12:07 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:21:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Dec 2025 19:21:36 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:21:36 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Dec 2025 19:21:36 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Dec 2025 19:21:36 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Dec 2025 19:21:36 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Dec 2025 19:21:36 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:21:36 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:21:36 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Dec 2025 19:21:36 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:21:37 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Dec 2025 19:21:38 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Dec 2025 19:21:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Dec 2025 19:21:38 GMT
LABEL org.label-schema.build-date=2025-12-16T18:18:49.430Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4fac8383dfc0031e7def1e69a9a7ae5a5694bf66 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.3 org.opencontainers.image.created=2025-12-16T18:18:49.430Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4fac8383dfc0031e7def1e69a9a7ae5a5694bf66 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.3
# Thu, 18 Dec 2025 19:21:38 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Dec 2025 19:21:38 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:21:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Dec 2025 19:21:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Dec 2025 19:21:38 GMT
USER 1000
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab29a47abbdeaf61355121afbe9d1cb9f8c108ec47a29b2d4afeb59a03f21618`  
		Last Modified: Thu, 18 Dec 2025 19:22:53 GMT  
		Size: 19.5 MB (19533506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4760ebb8abf91d561eefc069dc4a4e5a01db0b00018c55dd83b4d126710a1d`  
		Last Modified: Thu, 18 Dec 2025 19:24:20 GMT  
		Size: 371.1 MB (371080478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9776bf97841da8fa92b7c024378f055ee8f5373bb4017ae3b7344f40f5aba199`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b03d82e6c16a6090a58d2608e55e6d3843291a20b1949a45f5cd14332446d70`  
		Last Modified: Thu, 18 Dec 2025 19:22:54 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1a56aef65ddc158873e575941c1e69620000d1d74bc0659b6850a572bba6c9`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77cd7987f2200e083dff7ff16df8583eb0301f2a7bf8bf6c95bd9788621e25`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d65cf1ea4e9b537dd42bbb39d6169421252ae2d25d5bae5a73ad7dc2b0f55d`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dbd2a5347fffe9d53d3dcc08ff4e423ae0039656492fa23f51c3e05ee72faf`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 4.9 KB (4894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e002f3dfe4c596c8dec9c8ec21b5064037bc83fa7019244953d57cdb893379`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a124049c4f0bcaecf11227148293aee403ae4fad2da62faaaf663b388274fe77`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c52ec5ba1a6cdcf4ac08250406d192cfbc85c12bc14670cf8fff3bcb2c0eecb`  
		Last Modified: Thu, 18 Dec 2025 19:22:52 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2711adb55097662a5c89d7c18c673d0657ac71307a8af6637f93f6072daad59a`  
		Last Modified: Thu, 18 Dec 2025 19:22:51 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.3` - unknown; unknown

```console
$ docker pull kibana@sha256:6c1cb07da1614fd4b8682c03010fc0ec34d53bc7e788871df160df5c70c5c75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6cb3466003b3518217a4d6c74a5dfd7d5f8397529f66f615ec4440ab6f6b3c`

```dockerfile
```

-	Layers:
	-	`sha256:d25d6afbe751e4601f89b843b27685e6482cd767a93dd17906382677284c9891`  
		Last Modified: Thu, 18 Dec 2025 21:12:10 GMT  
		Size: 5.7 MB (5748164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53dbf7fd8d5fc8c9b1ecf25a555d5b76fd8a0840a52ad2e567beba26243677f7`  
		Last Modified: Thu, 18 Dec 2025 21:12:11 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6138819f06d15ca1abe96324f7c0963296e5ff4b1602ee7f3c264e12b06b6d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.1 MB (459081227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c42bc9b278032c743b64204e3efff36c45c4ac12833f008797dd1be4ef16e8a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 18 Dec 2025 19:11:33 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Dec 2025 19:11:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:18:44 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Dec 2025 19:18:45 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:18:45 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:18:45 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Dec 2025 19:18:45 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:18:46 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Dec 2025 19:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Dec 2025 19:18:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Dec 2025 19:18:47 GMT
LABEL org.label-schema.build-date=2025-12-16T18:18:49.430Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4fac8383dfc0031e7def1e69a9a7ae5a5694bf66 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.3 org.opencontainers.image.created=2025-12-16T18:18:49.430Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4fac8383dfc0031e7def1e69a9a7ae5a5694bf66 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.3
# Thu, 18 Dec 2025 19:18:47 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Dec 2025 19:18:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Dec 2025 19:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Dec 2025 19:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Dec 2025 19:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dade8cfe4db21a2f8b8aab23ff8d044030a4a7fdd1619b1c76c7ab4c544ad6`  
		Last Modified: Thu, 18 Dec 2025 19:20:07 GMT  
		Size: 19.5 MB (19492779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8989f9d46b39b6a93991bbd15e5756530f14219ed1f13a8d3565242eeefb412`  
		Last Modified: Thu, 18 Dec 2025 19:21:49 GMT  
		Size: 384.8 MB (384808754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48717da58176a2425cc342dfaf87232485e5f833dacc5b157fbc8a2cc4db647f`  
		Last Modified: Thu, 18 Dec 2025 19:20:04 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670e8f70618ff086cf95185f7f004039ed712dd9f4166d8789fc5223928c69b8`  
		Last Modified: Thu, 18 Dec 2025 19:20:06 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8943458722ce2392e8d59d6149e7cb9a16868ee8695808921c3d76647d6a1c2f`  
		Last Modified: Thu, 18 Dec 2025 19:20:09 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df1c459c380f9c4c23ae57ec41bf8e38c9e7713fb1f933ceb7536e66a79494c`  
		Last Modified: Thu, 18 Dec 2025 19:20:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60aeadb02085d77f21a7ed0f8c172cbad6d5c7e7057a2f08b5c4e028052b663`  
		Last Modified: Thu, 18 Dec 2025 19:20:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5720bd96c32bae56b8932cff8af558b4804f90eed74720fe459334541a9743b`  
		Last Modified: Thu, 18 Dec 2025 19:20:04 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6b8e74207f21fe9547e59e446a6a06a42b8d1ca04698ff34e604d29d29a3cf`  
		Last Modified: Thu, 18 Dec 2025 19:20:04 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1b2ec5524aec3db40c64fc51ae9168e16e2dffea5491a42d4e2c18e3dc820b`  
		Last Modified: Thu, 18 Dec 2025 19:20:04 GMT  
		Size: 73.5 KB (73451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e427744cdc4b5bc80e701919efc093bbca58cb1a463fb4a698fdbecba15264f`  
		Last Modified: Thu, 18 Dec 2025 19:20:04 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ae253a515c4df1e22c9a493e42e146acc387650a27e3d46503faae87517f7`  
		Last Modified: Thu, 18 Dec 2025 19:20:05 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.3` - unknown; unknown

```console
$ docker pull kibana@sha256:57e8d3fbbf702e9082f62c751c4fb259d4416f72aec560bda4054d66ce3ed464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179b855cc6bdc94083d40ec83baa5f7b5a05a961cdc6937fbf183ee55fde4015`

```dockerfile
```

-	Layers:
	-	`sha256:b61245008fad9d737a290a7da12517e45b7ddc7b3a6a24965125ed3c023cd86f`  
		Last Modified: Thu, 18 Dec 2025 21:12:17 GMT  
		Size: 5.8 MB (5750172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a39bc56f7a266301745e1a4f62f43fb9ee1476f896bacd726f553948e748b0`  
		Last Modified: Thu, 18 Dec 2025 21:12:18 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
