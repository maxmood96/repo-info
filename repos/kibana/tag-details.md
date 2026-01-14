<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.10`](#kibana81910)
-	[`kibana:9.1.10`](#kibana9110)
-	[`kibana:9.2.4`](#kibana924)

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
		Last Modified: Wed, 14 Jan 2026 05:46:37 GMT  
		Size: 9.4 MB (9446173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1853a381f41232f921e5526c3e6700154b827f6949ce80249b881bc6d699cd09`  
		Last Modified: Wed, 14 Jan 2026 05:46:34 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a760837544bebe14a33bb967a1935d4a4d15c3abb9227281080d71dbe975e53`  
		Last Modified: Wed, 14 Jan 2026 05:46:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6922bd60bd5fec7692b52505f3a4906334bcbb68e40c63f2ec9e47f2af918012`  
		Last Modified: Wed, 14 Jan 2026 05:46:36 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89931a8edb2c8dbee44c71f14803f8136f4ec18de1703d9337b4641620485f85`  
		Last Modified: Wed, 14 Jan 2026 05:46:34 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf67254e8331c96e4c2f96142859368e57085c91814b2f0e300934367be2c05`  
		Last Modified: Wed, 14 Jan 2026 05:47:03 GMT  
		Size: 311.1 MB (311148121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55926e73b726f9b587823eac64e2486adf2c4bc7eaaf0dc86a1823587916f465`  
		Last Modified: Wed, 14 Jan 2026 05:46:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f1fee166071308bd9f88d3a9c288789bb822f58d513126237e97547bfffb71`  
		Last Modified: Wed, 14 Jan 2026 05:46:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12355655218fe6c3b48187926fe316193619b4b7b9eae9eab2d102d577d00a30`  
		Last Modified: Wed, 14 Jan 2026 05:46:34 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a729783706fcbd9ef444378dee2624e0fffa33a4213baa8a774ff08d00b3d2`  
		Last Modified: Wed, 14 Jan 2026 05:46:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3565fad2095d35954b8261412110b44af400bcd11be235b398ae7faf5599bc`  
		Last Modified: Wed, 14 Jan 2026 05:46:35 GMT  
		Size: 158.0 KB (157999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54760310f932ac7c65ec67da5c9eb6f576c221ed4872eb417a199ea2a76978`  
		Last Modified: Wed, 14 Jan 2026 05:46:35 GMT  
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
		Last Modified: Wed, 14 Jan 2026 08:07:06 GMT  
		Size: 4.9 MB (4856890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30130bbfba23015d367d7aeab62a8d79e080423b3f708b6eaad4cfa1d184bd66`  
		Last Modified: Wed, 14 Jan 2026 08:06:38 GMT  
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

## `kibana:8.19.10`

```console
$ docker pull kibana@sha256:d092138e468cd0a5ab52074cc4884120a952b29ac076eff63d4f9a791ae8233b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.10` - linux; amd64

```console
$ docker pull kibana@sha256:65fbfeb57f805a9c6819b5b63dfffd76c6345ac414368367c2a1b6450997eb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.9 MB (440927435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef2ab40005eebd9fff259eb4af129e99fd85645cff550334458352997e881f1`
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
# Tue, 13 Jan 2026 19:05:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:34 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 19:14:37 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:14:37 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:14:37 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:14:37 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:14:37 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:14:37 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:14:37 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:14:37 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:14:38 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:14:38 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:14:38 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:14:39 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:14:39 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:14:39 GMT
LABEL org.label-schema.build-date=2026-01-08T21:22:46.611Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6803805478ed373f560b161907994536f4cafef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T21:22:46.611Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6803805478ed373f560b161907994536f4cafef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Tue, 13 Jan 2026 19:14:39 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:14:39 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:14:39 GMT
USER 1000
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada8733a9d648dc70bf2b39836550d6dbb8440082257baecbbe7ef21c038b1dc`  
		Last Modified: Tue, 13 Jan 2026 19:15:50 GMT  
		Size: 9.4 MB (9432482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388a55e5094643d296f2e16b28d031bbaeb3f1df34e86824e95dbf0feb47ac13`  
		Last Modified: Tue, 13 Jan 2026 19:16:17 GMT  
		Size: 385.1 MB (385126542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff2bf0727ddfc0eb22b9cee52c6add7abadf569b221ae1e492727992d5e279`  
		Last Modified: Tue, 13 Jan 2026 19:15:49 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a50b5970895bb84aae7646dce57ee8e70c3591483340d9ce1f50f36d70e3588`  
		Last Modified: Tue, 13 Jan 2026 19:15:51 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868083bddc0e2757b3ba65eb26082387ba03e75b7a81cab850a6672e172f76f9`  
		Last Modified: Tue, 13 Jan 2026 19:15:50 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874549162ecb535a5596c4386cb31dc8525be3ce02e074de13f27f18fec01b41`  
		Last Modified: Tue, 13 Jan 2026 19:15:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f806443f2d6fb25173d863c16ff638b539994942ccac51dcb6f6a0a425560e8c`  
		Last Modified: Tue, 13 Jan 2026 19:15:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9f1b8bbde6cdf56e17283de45ca4010f692bc75cfea26ae43cf3e736ee5bbe`  
		Last Modified: Tue, 13 Jan 2026 19:15:49 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab47bbfc6cd72a130ea23883f1bebd68d94ed92a715786db211c952a7312d9ec`  
		Last Modified: Tue, 13 Jan 2026 19:15:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bb6cefa89c1a6505f95919f5acc4a9359103e35603f8e7d38e31625ab9e96a`  
		Last Modified: Tue, 13 Jan 2026 19:15:49 GMT  
		Size: 161.5 KB (161460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90824f3385acf7a59e925fc1ee1193858cae19c0465487d04fb606ef8b60230`  
		Last Modified: Tue, 13 Jan 2026 19:15:49 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.10` - unknown; unknown

```console
$ docker pull kibana@sha256:a8efb3e530d42ee93d60e5e2acca9cac9da440733997e4b13f0376674e4bd4a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91299c4514c3244979c0c6de9b7640796ddbad59458748045dae475e9dcc3c12`

```dockerfile
```

-	Layers:
	-	`sha256:d2fa4a5d26ca248139ef882b22f4299bb714735c32200397d80a27db53c6f34a`  
		Last Modified: Tue, 13 Jan 2026 21:11:24 GMT  
		Size: 4.9 MB (4919875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf31bd454f2d54eb4927386efcdfef03e22c49895072efe23049f0209572480f`  
		Last Modified: Tue, 13 Jan 2026 21:11:25 GMT  
		Size: 40.9 KB (40914 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2409eb385be4bd60b150d022b872894903b46a1c64aeb4f124ebc65c21b0d866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.8 MB (453800298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61489634065fb452c462df8defd89feaa97a0c998c7c3bcd9c73daba79e87aa7`
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
# Tue, 13 Jan 2026 19:05:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 19:12:20 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:12:21 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:12:21 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:12:21 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:12:21 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:12:21 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:12:21 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:12:21 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:12:21 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:12:21 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:12:22 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:12:23 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:12:23 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:12:23 GMT
LABEL org.label-schema.build-date=2026-01-08T21:22:46.611Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6803805478ed373f560b161907994536f4cafef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.10 org.opencontainers.image.created=2026-01-08T21:22:46.611Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6803805478ed373f560b161907994536f4cafef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.10
# Tue, 13 Jan 2026 19:12:23 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:12:23 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:12:23 GMT
USER 1000
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ee1b2ad6896107b06fa52fc4f59ff79b8f9cbf47d60dde0d9a99b55d7bc41d`  
		Last Modified: Tue, 13 Jan 2026 19:13:42 GMT  
		Size: 9.4 MB (9446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ac6baa8fbb29e8b2bb854a1f0f43779e6da53b603fd1445c41d8389cb239e2`  
		Last Modified: Tue, 13 Jan 2026 19:14:37 GMT  
		Size: 398.9 MB (398851793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa73d77cae2fe85c9a229fe0fb2a483135bcd9ba372fa47a053efdc335d854d`  
		Last Modified: Tue, 13 Jan 2026 19:13:41 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a592f5ba5e1f04b090b252e24027ca9a86f3b03c964110aac3aca1a37a797437`  
		Last Modified: Tue, 13 Jan 2026 19:13:43 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4ea191c845667203db9aeaccab09a2116cd5948bec606d83890072b87e1e9e`  
		Last Modified: Tue, 13 Jan 2026 19:13:41 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f67216c0ffb2f3a4cc2f119dc6e3ef7926a1615f945c5aa0549193de686a99b`  
		Last Modified: Tue, 13 Jan 2026 19:13:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3d4af35882c854895daf21480b60a3dc469dd2d83df36ff69632f542a543d4`  
		Last Modified: Tue, 13 Jan 2026 19:13:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d987433401958c74a430f1fe5f81db44b8b89e518314e7f990180e4a74a2b6b3`  
		Last Modified: Tue, 13 Jan 2026 19:13:41 GMT  
		Size: 4.8 KB (4815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c5b23289c3a578e5d31190366c7406a5442ae4d1d88f96e4b8e7d6a977794`  
		Last Modified: Tue, 13 Jan 2026 19:13:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516bbbca7e03729500337e2c3a4eb6b03048151bf95f644eee930a33eea08567`  
		Last Modified: Tue, 13 Jan 2026 19:13:42 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da6b0784cdc93dce2abee0cff7dc26aef951460bd54a2389a7f76cd4bd1da7c`  
		Last Modified: Tue, 13 Jan 2026 19:13:43 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.10` - unknown; unknown

```console
$ docker pull kibana@sha256:5e48c1478494583232e7fb6cd6b27d942af447d149419b49b88a7658bc25c23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a192ef2d30ac09b097744a8ea8c5ee23d9b9bf1a57864fe8b624df65cfef133`

```dockerfile
```

-	Layers:
	-	`sha256:c4cbc1244a9ea062b8bf6d828a5fc639521373c30065327f15825c79b5aab803`  
		Last Modified: Tue, 13 Jan 2026 21:11:34 GMT  
		Size: 4.9 MB (4920939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a8508af8d431bbbe8ca66134ed385520046ae3d80d33f5f5065c19f73b781ff`  
		Last Modified: Tue, 13 Jan 2026 21:11:35 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.10`

```console
$ docker pull kibana@sha256:92659a0af9332fc3115b12348473709994cad579c1ed28f738b89ba3c45a77dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.10` - linux; amd64

```console
$ docker pull kibana@sha256:6d55ebef44242abc57476edd335c510ac16a905476d360f4a16969d4e23cd36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441416565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d22e7d6f23e07359059c8ae816b86370881039e07c02de18450eb49876791e7`
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
# Tue, 13 Jan 2026 19:05:15 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:13:45 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:13:46 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:13:46 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:13:46 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:13:46 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:13:47 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:13:47 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:13:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:13:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:13:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4bc21e5de8adf1269e10e4e48cbe203a2e5daf830d703e20e99172ae58857f`  
		Last Modified: Tue, 13 Jan 2026 19:14:56 GMT  
		Size: 19.5 MB (19530147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19903af0dde482fbc9576ed9d0a3df7d0b3d3b87a16c4ffbddaaf143307c35ca`  
		Last Modified: Tue, 13 Jan 2026 19:15:04 GMT  
		Size: 365.3 MB (365287415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913a81407a2be3a11cf45a191fd443cef612f508e51cf4e580bc76adbe1c636`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9446220ea6a418be5dc5754de5228ec08cca75eec99693ecdd0bd8f72fe9d8b7`  
		Last Modified: Tue, 13 Jan 2026 19:14:57 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a31fa8bab6b5b488e96f7a463584c15982a9d1270c48fde9e8a162ae87220`  
		Last Modified: Tue, 13 Jan 2026 19:14:55 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f274bc2c4e97f1aa92fe3ab520f6733ea75637bbc4721b4d32cad7efa5464025`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab827071fc434fb8ac3d65438c819e2dfedd2455ec2fce0157d49e8752bc1c2`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae69bf708487ae67a5591c54fb34bfcdba2c1ee8bcf9b564ec14f8152e62594`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 4.7 KB (4743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4298a6de0d2303414159d0e45b04257522121a47498fa5e77fc61daace04c35b`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c58ba0d8485a45c7aa910d161858535c638abb02c94d1d242e07e5887477671`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b07e6c36b3fb4b13b9f849605db0f2635492d27ab113659a6944e3430cbc963`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc30e68fdb557e7573a75e3be2d8282a2947127b87140cc2ab3a9e0ffdc170f`  
		Last Modified: Tue, 13 Jan 2026 19:14:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:9cfa1faa6d75f88ddda33449be78da06466f049d137b3cf43b038fe0db65e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5718269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78edb067b5bdaea1adefa46a43faec793e22cf394e5142c97fe6ad789d8c25f7`

```dockerfile
```

-	Layers:
	-	`sha256:f064fd63cca4731797d7ed3dce6d8ebf5dc57b1d280b0c5c37cc36d1bd5d7034`  
		Last Modified: Tue, 13 Jan 2026 21:11:36 GMT  
		Size: 5.7 MB (5675036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e9a427827af141920bee46a3c2b45bc6d92fc809ce6aadabf3873b8f3154d7`  
		Last Modified: Tue, 13 Jan 2026 21:11:36 GMT  
		Size: 43.2 KB (43233 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9dd0d5c27bbdf5592d3028ea46a41fef0b1cf2bd57f16b71eb7623f28e65a1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.2 MB (453245696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38861e4f4846a6fad4c30e75f05094ee76e8c9c659f7047f2f38d2d9791df779`
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
# Tue, 13 Jan 2026 19:05:30 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:30 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:12:55 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:12:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:12:56 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:12:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:12:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:12:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:12:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:12:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:12:58 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:12:58 GMT
LABEL org.label-schema.build-date=2026-01-08T12:24:56.202Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3c5e7066866006c39ba40861ab0c05b6406ed357 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.10 org.opencontainers.image.created=2026-01-08T12:24:56.202Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3c5e7066866006c39ba40861ab0c05b6406ed357 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.10
# Tue, 13 Jan 2026 19:12:58 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.10 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:12:58 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:12:58 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:12:58 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:12:58 GMT
USER 1000
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9c0dfdf5c8970a5c67c4c352a3ca8842ddff4d8adadb3f6fd4f9e227f399d`  
		Last Modified: Tue, 13 Jan 2026 19:14:22 GMT  
		Size: 19.5 MB (19479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0675f37826a3a24fe5ddf889f8116a9e64b57f2a39febe9f679364a4db6a56`  
		Last Modified: Tue, 13 Jan 2026 19:15:08 GMT  
		Size: 379.0 MB (378986587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e645d82dbc194239a72b2b6fc213e8f887f5a79272358466f2a47f7c1ab5d1f`  
		Last Modified: Tue, 13 Jan 2026 19:14:17 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb44ba49a5b4b8418e4efc914345d8e2f3802952d6631f062a3609dd312ff25`  
		Last Modified: Tue, 13 Jan 2026 19:14:19 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518cad7b7c64e5232478f71730dd7c2f0c4e2e22db9f2ab4db237c0a477180fb`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662e6d71d830b9f06ca4ca97d6fae8f8e420737d8423cc5ca6812e48d02a25a1`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1699c3a8ddb6e71e4775eee7dc931bbaed51b40eee9159141367c2edf10edf9`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206d6eea901e3724603a18076b288f1a6b89390b552422b7c0b3add60c26662`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 4.7 KB (4745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec7191dd7cc12a99ce9c07f5daaf537de54941c85d2eb594912c8ee3f4ce990`  
		Last Modified: Tue, 13 Jan 2026 19:14:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563e7d6683cac25caac1aa1562074e5dfd4225a3842c5a2a6be2bb58208c7947`  
		Last Modified: Tue, 13 Jan 2026 19:14:17 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4f2b4e45c56cfc16217574d813ca8aa904158bbdb679a00e319525baa100f9`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2958589136402310dc82339f43f0feec6756d724cb401c9f7d3efb2253b63c`  
		Last Modified: Tue, 13 Jan 2026 19:14:16 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.10` - unknown; unknown

```console
$ docker pull kibana@sha256:61d741d2ecd5b0e12e98bb0ca281d255da83b8bc9a495160df31332b3ab22cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7558bbf2991c66fd0d9bbe704a6f0e21adaba7fdcfae8b01cd00ab0cc79ca9f4`

```dockerfile
```

-	Layers:
	-	`sha256:c16292918cdc0d579be52c52518b58131ea2dd51f30ef0e761e53df52ea91b0e`  
		Last Modified: Tue, 13 Jan 2026 21:11:43 GMT  
		Size: 5.7 MB (5673708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dccbbfa37d4996dc0bf057db73154801a5bb9949692ea2d515daeebcb89286b`  
		Last Modified: Tue, 13 Jan 2026 21:11:44 GMT  
		Size: 43.5 KB (43490 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.4`

```console
$ docker pull kibana@sha256:d2302b46ae4e582ae6db41e8943bf47dfef7c7dc337417ce6dadd51e82ec8b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.4` - linux; amd64

```console
$ docker pull kibana@sha256:c87190bf981f204ece46a242b1364e77a7d1f590e7e8df235c1ddec7d9ac9ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447476824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f01d3cc1cbb7ce592a2e2eeecd147a89bc51a7db323385a53b8a424ffb35816`
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
# Tue, 13 Jan 2026 19:05:49 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:05:49 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:15:04 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:15:05 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:15:05 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:15:05 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:15:05 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:15:06 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:15:07 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:15:07 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:15:07 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:15:07 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:15:07 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:15:07 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:15:07 GMT
USER 1000
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f15fa39de48b205531a45ca6d6cda8094d4a06a6502acfddc34895d0b2643c3`  
		Last Modified: Tue, 13 Jan 2026 19:16:25 GMT  
		Size: 19.5 MB (19530112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dc175bbdd032134742011038dc122a2f03b2e439bcd7c8bd91302ca8dade07`  
		Last Modified: Tue, 13 Jan 2026 19:16:30 GMT  
		Size: 371.3 MB (371347565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb1920e9b91be4482a4007ae49dfc49b2dab20c8e703446ac086944247291fc`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe27caa33b43e2ccdbdd0014afc01f7312bd84a29531de9e47b5c93199dfdc4`  
		Last Modified: Tue, 13 Jan 2026 19:16:22 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e13713225303673880e773df8bb6d666655cd9fa2806fdcf9981a0874c0f69a`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec254fefde6ee4be8512701f842bc8c140c62de5a73b71e11f28a11c22727f7`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4ac14c149cf5d7c0efc5314780041166f670cece91bce6a985508fce24ae2f`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17ac5dc97322d3d4b0e23a70bc65b5b972a6b65ffe456744691b1e5ee629efa`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d659e8c3c8f5107f7ef2fa99a0ff03931440975b7b2496891b889249fd44a0bf`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab23b595a9fdc547ae2335b975d908db471bb1ca9fa7aae35ae5d170c77bf969`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baff20cf038ab062e6d0d73811bfb48cc11f10a5710d053ec8f14f49aa3b448`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7cf17a1c63aaa06502a03a33622b70549c07459ed7b8c3b04d8734b1c6c3a1`  
		Last Modified: Tue, 13 Jan 2026 19:16:20 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:4057492ef88b0ddbc6ea82e62b3ec7b47501b141cbc56d7a98ae90a8eebed80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64dc46fd0ac655ebf17dcf9b5bd44021e1b28f466a7c7023ff641f6a1e1f26`

```dockerfile
```

-	Layers:
	-	`sha256:e31fa34ed00a30baa744230e581ef08b01d97f6f0b729695657774e753610c2d`  
		Last Modified: Tue, 13 Jan 2026 21:11:45 GMT  
		Size: 5.8 MB (5750291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2843fa70f64fc60b6dbe28ad123e374166ab20444b78a60f83d9a4c46877b41b`  
		Last Modified: Tue, 13 Jan 2026 21:11:46 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:792f79b198075221dd70b8bc3ad31e32dff279fd882811f4af6ebc7ebf2ecd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.4 MB (459361329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed87099abba59416d6aa4391ecf49438e67a8462aa0ccdca1e09ff99f59f2646`
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
# Tue, 13 Jan 2026 19:06:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 13 Jan 2026 19:06:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 13 Jan 2026 19:13:39 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
RUN fc-cache -v # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
WORKDIR /usr/share/kibana
# Tue, 13 Jan 2026 19:13:40 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 13 Jan 2026 19:13:40 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 19:13:40 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 13 Jan 2026 19:13:40 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 19:13:41 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
LABEL org.label-schema.build-date=2026-01-08T21:40:45.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=b05a85503d4590280c7e9263175269a5f4a09729 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.4 org.opencontainers.image.created=2026-01-08T21:40:45.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=b05a85503d4590280c7e9263175269a5f4a09729 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.4
# Tue, 13 Jan 2026 19:13:42 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 13 Jan 2026 19:13:42 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 13 Jan 2026 19:13:42 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 13 Jan 2026 19:13:42 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 13 Jan 2026 19:13:42 GMT
USER 1000
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6dfe0b549339ca1d6d59332208080f200e2457e4b7f6d9dd0da4b481dbf361`  
		Last Modified: Tue, 13 Jan 2026 19:15:01 GMT  
		Size: 19.5 MB (19479548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8295c4a80b890d6044aa7979972b80ab7dbeb5b2a3b878e83ffbfc2d5bacefe6`  
		Last Modified: Tue, 13 Jan 2026 19:16:23 GMT  
		Size: 385.1 MB (385102079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2358211d34c8d307119843cc6d1a9b1e325d8230357308c5b438b6749c19357`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f299218803ee977a72f4326dda1e0b81b2ea311f0dc7cef17741887f0c5a554`  
		Last Modified: Tue, 13 Jan 2026 19:15:10 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404f77b7a0e385f70f3528ffd525e5b6edb4993c35e0225793db07efbb95b585`  
		Last Modified: Tue, 13 Jan 2026 19:15:06 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf91a8c6051786a1b706ba20b41d963980f16bdddd5e952d75dcfee16f4a50d`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1bd4de5efdef4a3b69fbf5e376f43187e316cffbb1be32a83a99151afc8eed`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568dc4c0c64804981aeb2a2f332de403da9dfa65f37fe894f2380801c65530f4`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f1df4183608ec3c0f41fb66231a38ef2a99e3aab23edc34fcef118366eeeb7`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9690d7cbb2e2dcc8da03363c9cc9e17028d712e83bf2304b7d60d5ce1c167e`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f2219d46c8f7e50444170a7d7b6b1d8b5e62815b4c7b44c81e9c499c73bfaf`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d985d907b280bdbeafa80861bbcfbdf91d43e5ab08f4ecc1b1a33c411e590428`  
		Last Modified: Tue, 13 Jan 2026 19:14:59 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.4` - unknown; unknown

```console
$ docker pull kibana@sha256:3fe6873a9f972c7b1cf92685f345cf6b62bccffc9859da32d7ac084015dd6478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecad4edf883d9c5e7e90b741c79553831c5108f7b6a35cb53e83237504bab9d0`

```dockerfile
```

-	Layers:
	-	`sha256:f3e4b713f2e8ce5a08ed48831268d2956b2ad2070ebe5ba598888e791ada22aa`  
		Last Modified: Tue, 13 Jan 2026 21:11:52 GMT  
		Size: 5.7 MB (5748963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f53931f09df7827f07ccff63266be390264ce7745eeb1ad1f2e17067f6e72c`  
		Last Modified: Tue, 13 Jan 2026 21:11:53 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
