<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.7`](#kibana8187)
-	[`kibana:8.19.4`](#kibana8194)
-	[`kibana:9.0.7`](#kibana907)
-	[`kibana:9.1.4`](#kibana914)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:6d5ccfeaed3067b9326199eabc4d9ef4cf6e6fa3beecb2aa7507bc001b736137
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:8c077b790e8ed307024e950f63169a8423a9118eea742d3b2c1ba2bf3c6cc1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353911510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a502980c08af4d35aac3cc6c1351bc4f634c53976877f6ca0cfcf89edcc27d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 31 Jul 2025 10:41:27 GMT
ARG RELEASE
# Thu, 31 Jul 2025 10:41:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 10:41:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 10:41:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 31 Jul 2025 10:41:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN fc-cache -v # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
WORKDIR /usr/share/kibana
# Thu, 31 Jul 2025 10:41:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 31 Jul 2025 10:41:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 31 Jul 2025 10:41:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 31 Jul 2025 10:41:27 GMT
USER kibana
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce7a9ecc935c9018ccc1770178b11986729441325b347f6a0ca2cdbd9abfb48`  
		Last Modified: Mon, 15 Sep 2025 22:25:19 GMT  
		Size: 9.4 MB (9431929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ad9b75ffc05c147455da48591847b1b688b27ce3beb143a0542c623505599`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c8b18c19270140ee63388cb260ccb5f852ca92b802daad6cf7669e72ab86a3`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd355434a97ddb6174c09eab64be756129a6b52a0ba65d24a524965ed5d3e03`  
		Last Modified: Mon, 15 Sep 2025 22:25:03 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc3b9669d90d4ba6fb3888bf7d7241fcd2767868e67c25414c9dc4ae3dc635e`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66785adf8849e0c3f854c7dc79aa8a7519ad43bd0f028f1dc855fe6189ce403`  
		Last Modified: Tue, 16 Sep 2025 02:13:54 GMT  
		Size: 298.1 MB (298112549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7a4a1f970c756ad6e34e323a4ed089d77872e82849b78c168d96015ec53cec`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e75e8397532b2b0936912911441bae590a4309be67e3a451e5c0281567c8a0e`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a41ed6b48d656d28ae80be03923f90412aae6ab6fc4316d6cc1b46aca72de6`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 4.5 KB (4502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a186bb1fb63faccadc32d85e70f3f9cbf83188bfbe3a2933757c93d98553e8`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e56a482f274a08b5aa7db229f481c2dee921c61f5b069ee80d1e43e218006`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 161.5 KB (161454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6971b6b93ec394b47b570ed7a5501fb3568bc04044580a423b24cb5a788e2d3f`  
		Last Modified: Mon, 15 Sep 2025 22:25:02 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:81a5b2f7be311d55baceb4c214709888f845f45bd36c8f0bed10188b7f02fd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50092b40efd3cd81f110cc7b2e477f47ef20ef7ffb796d09ed069e664a0e54d9`

```dockerfile
```

-	Layers:
	-	`sha256:9d451f2b8a7dd90ae424e1cb022f6e170b55978f853216d8b4a47ecf6de5ac8d`  
		Last Modified: Tue, 16 Sep 2025 02:11:22 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852e72838fdf1197f8b13366ecf21c48b98290b5983d012fd1bd9538780acdc4`  
		Last Modified: Tue, 16 Sep 2025 02:11:23 GMT  
		Size: 44.6 KB (44554 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9510cc0c81ac8b4b25d4984ed3c8390f76ec6a0d600a221a467e910f9f23b660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366095149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46185905f960632bc42434feffc14a369d47479ea98c9ccc5e5bc8f2944509a0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 31 Jul 2025 10:41:27 GMT
ARG RELEASE
# Thu, 31 Jul 2025 10:41:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 10:41:27 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 10:41:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 31 Jul 2025 10:41:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN fc-cache -v # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
WORKDIR /usr/share/kibana
# Thu, 31 Jul 2025 10:41:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 31 Jul 2025 10:41:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 31 Jul 2025 10:41:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 31 Jul 2025 10:41:27 GMT
USER kibana
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2717d3cde729f3d3e5b32a6f7ada6218a8f118626c640c692805034313cdac7`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 9.4 MB (9446013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3428fc07e1b3668ae90f05c142156aed1e7d4fe1feee24843b4aee2d654881`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8adc9f2502e8c21149d0112861f3ce3afe4e1a5ec551fc5450421667494eb85`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f40d5c17996f26bc2b4d9bfadde9fb26b403e52d2114215759aaa5ffe915a6`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2603bdae1a380ed55b07f587e41304962a866654baadcfa97a43bbd1aed4c04c`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 5.2 KB (5246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7672aec4ef4a2beac729712cae797429322d20740a447bb2af0f0c14358fa38d`  
		Last Modified: Tue, 16 Sep 2025 02:13:36 GMT  
		Size: 311.1 MB (311148128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f3aae84600988918933c95084715b72c51dece35f3c65211e1390646ff341e`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90105c1751675747859a5c8a21bdf9da55279dd7a99225b4ecd06aca92dcf7b1`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21feaa0f174d406f9b5c9ce1d7fe17791cb1c591e133968fcd0d7b95d0a4f629`  
		Last Modified: Mon, 15 Sep 2025 22:21:37 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000c2914a489b0b78e018f7b55f3a6526effa135150168deaec40efff482328e`  
		Last Modified: Mon, 15 Sep 2025 22:21:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb33da1196776ec5eb53ee963b5c158170b9b7de862c670ead43f9920596a2fe`  
		Last Modified: Mon, 15 Sep 2025 22:21:40 GMT  
		Size: 158.0 KB (157994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c638875352fb0763be06203041cbd5b83598f3b100fc18f12597007b67434b3f`  
		Last Modified: Mon, 15 Sep 2025 22:21:41 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:4f3d6f565d47fe97d14258f9858db3b705002b049d002326f22e15f1a8f8a7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a92f0bf708c744468013766661179761e7af28feb67d3219d2c64ecba9cb906`

```dockerfile
```

-	Layers:
	-	`sha256:4a3008a49d1b6d5f43429b262c0c06a9fbbef2264c06a01b86f8da689d550424`  
		Last Modified: Tue, 16 Sep 2025 02:11:28 GMT  
		Size: 3.5 MB (3507898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae45d9675ef50617e48dd063fa050b88929937c04ee49367e33d862b9b80d2e7`  
		Last Modified: Tue, 16 Sep 2025 02:11:29 GMT  
		Size: 44.8 KB (44832 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.10`

```console
$ docker pull kibana@sha256:6eea28af2ec07a16743e788ec15dffc92d5d0af6c73747eca3d69a20ff305d07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:44238afacf7d44dadf439be01ef21bd37700f2e0c5071cbacaab5345e1367239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403301764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575d693af39c96bb672e2759ee54eaf4db0d37ea9085ab5f574b89f8b7ae73f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:18:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-07T20:18:34.689Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-07T20:18:34.689Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed8d1f45f9020b85b5181ad0aeb9812b36f1d74f06f6ea8da5d77c254064363`  
		Last Modified: Mon, 15 Sep 2025 22:27:34 GMT  
		Size: 9.4 MB (9432038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe00be9766b15485a0cfbe5c59cd71a44d701e70d493861e4d43da3271e9b746`  
		Last Modified: Tue, 16 Sep 2025 02:16:40 GMT  
		Size: 347.5 MB (347502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac41dcab66840ae15727463fd022227b2248bda392adf917032a951e0752db50`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56ccde6fe5e4ff3c04248052b164d3cf70e981de190435a2d8a6beb2f004a7e`  
		Last Modified: Mon, 15 Sep 2025 22:27:34 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd734d4f09987cb9459d64e5c09db07f5619c69abc44a2d5640fd6ff682363a6`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4912d7eb41415bb7243053e84928b5fdc559230ab3345215438e6f9cc343ce3`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4175fabb12ef89237cb1f663c8032615c19b894583685d9032d2ec202d2e60e2`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48be88743844ca7d3c5906478f7022b45046530a894c5afeedfa5dbb850f705e`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e585404e59a319bdffb6762a7c3cbcac99685e6464d6fdcfdf1735a4f773ad6f`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f18357d46a09d2f911f63af52af512619d862991c6526262a3eed58c0d90a5c`  
		Last Modified: Mon, 15 Sep 2025 22:27:32 GMT  
		Size: 161.5 KB (161454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a5b839b03d2a92323a1ba26f930fb798cd47768ed192d336a01c4187e7a6dc`  
		Last Modified: Mon, 15 Sep 2025 22:27:33 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:c049fde25cf169b285378df1ff52dd46a9ab20d8efeb31706e50b49f01805692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585138c6cf5167dc074be0c41e889ea52973996e4f696396eb766d359b3644bc`

```dockerfile
```

-	Layers:
	-	`sha256:f993b28ad7c68907d24ff187bd1b999ad0df1d54b9c803a72c7f87f2fdebfe36`  
		Last Modified: Tue, 16 Sep 2025 02:11:33 GMT  
		Size: 4.5 MB (4520140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00655392f83aa0d998b822806c325d0e52fc32bca8bccf8fe4a73ec9d6f32bf9`  
		Last Modified: Tue, 16 Sep 2025 02:11:33 GMT  
		Size: 40.7 KB (40734 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b90c644a50fe27a8e617643ccb64efdf89da75b4b0505767a0f38df3ceefb083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415498712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4112b7983a589d979c81c0ae28cdd5fa1f96623e82271d233d8412d8e7aa8c8d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:18:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-07T20:18:34.689Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-07T20:18:34.689Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734709754546c5943e209dedb0d3d16c8f96c6b10214ae9a5de4a6b9c4434237`  
		Last Modified: Mon, 15 Sep 2025 22:25:42 GMT  
		Size: 9.4 MB (9445984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da1d730b43fe96d4e581e11c29585ee1fcec369b3034421ab758c8d30cef64b`  
		Last Modified: Mon, 15 Sep 2025 23:20:52 GMT  
		Size: 360.6 MB (360551692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c86b2b982feadc6822ddce1dd4f429f02cd9155ae6b973aac43ad4618a1fa3`  
		Last Modified: Mon, 15 Sep 2025 22:25:42 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49493a662ec53e6e11a31df5e3ffcf8a370fe744dcce227a97acb6927c12ce77`  
		Last Modified: Mon, 15 Sep 2025 22:25:43 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ed969047e7b83382619958c77659e456808d39077c4e103ee3e634e8602df`  
		Last Modified: Mon, 15 Sep 2025 22:25:42 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bab73921c150f614adbd3f7c469e6fb2afa1627ce6d208c2a2de4e23139d3`  
		Last Modified: Mon, 15 Sep 2025 22:25:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0814f1ba29078aef3c3e0af904fa77f7f9fc1c0a498468744001c88907fa3b17`  
		Last Modified: Mon, 15 Sep 2025 22:25:43 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c61f788321015efd7c576ea0d8905bd8fa3048294783d5c23fcd733a5b5efb`  
		Last Modified: Mon, 15 Sep 2025 22:25:43 GMT  
		Size: 4.7 KB (4729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c715615205ebdf6813d5ea978a427ffc862c08cb47b525f2e3293d7ebaebbae`  
		Last Modified: Mon, 15 Sep 2025 22:25:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd09d4ffc44f34ca889dca25280fbe8ae285897129fc304cafbb9e036cb331a`  
		Last Modified: Mon, 15 Sep 2025 22:25:44 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1578dc3b28e00dafeb92eb0965cedffa0417ff974022e25def4e499afdf8a5a8`  
		Last Modified: Mon, 15 Sep 2025 22:25:44 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:6c17fd9373ed35f2d9fcd6cc43d8e9b28efb2ef0561e7159c2627d880fe2d06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4562185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1a2988865063cd13aec5ad8e906047f84f3634d9e4fc7ce38ef220b2ea956c`

```dockerfile
```

-	Layers:
	-	`sha256:87d21dc323db106d21343792bb96e5439e919fc74c04bc5fe62ca37feec4e4ac`  
		Last Modified: Tue, 16 Sep 2025 02:11:38 GMT  
		Size: 4.5 MB (4521204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972e56cafa62ff0e0af730b5bcc29c33ca7b6b1ca15c786664285c18a5cd1d86`  
		Last Modified: Tue, 16 Sep 2025 02:11:39 GMT  
		Size: 41.0 KB (40981 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.7`

```console
$ docker pull kibana@sha256:1a735d2d3e1387689dff58d4fefead7d691e5a761351c630b5563a2555ab4790
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.7` - linux; amd64

```console
$ docker pull kibana@sha256:6aea27bfa3d82e8d91cbc7cece97debdc07b3a40ca8aa3857ba5a335fdccf714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.1 MB (424060436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a4870148670ee160a9064ff06b2848b374f25a4a1fade4d75b98ee2c6bfa23`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T20:18:41.039Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T20:18:41.039Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36fa4afddab95148c7af59007a1f58d4478ad91cd8d704e4ffb8a3ff1a45d6f`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 9.4 MB (9431941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1f1c393f52384bb9dafa14786588da009bb517817d8259b4714126c2984d2`  
		Last Modified: Tue, 16 Sep 2025 20:16:25 GMT  
		Size: 368.3 MB (368261404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea93b49b0ef51e8039e8a5d44ab8b79af23176760581fdbb52fef1390fa0c3dc`  
		Last Modified: Tue, 16 Sep 2025 18:08:34 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9a7c685e14192461c16832c186875764e3d3c4cd8d23b9e70dbb99efa3f282`  
		Last Modified: Tue, 16 Sep 2025 18:08:37 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372df1bfdaa67954a145b2c89f3822f34c818210d5029917957814c399c9e783`  
		Last Modified: Tue, 16 Sep 2025 18:08:35 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715b588be7e19d8ae37c03c757cbcb01bf78b1f303982083a08812468e7e89c8`  
		Last Modified: Tue, 16 Sep 2025 18:08:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a219996342d11019b85782c2dd6864fb745076a3cce167cfceea01796506ecb7`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6ba89a5481523fc75f4a4fecfd866d881feee97683541e9c3ecada0cee646b`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 4.8 KB (4758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1f5a4717be51d139af45bdb234a70298b52eabc4f6ef9bae817c439a9970b3`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b861e625bd98b3683ffda27d05437258cc5f9938d0e5be487043095b11a84f1`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049214e99d7d44c89275c812d558b5d207799e95c3be6100856bf6a5b3897d2e`  
		Last Modified: Tue, 16 Sep 2025 18:08:36 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.7` - unknown; unknown

```console
$ docker pull kibana@sha256:e69f1b8fa5cf4cf1d54e7f647f421a36b24194ffdd2fe67625e81eb20efe0f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81db3c7432307223f82529d76a45f8cd1ab66aa9b184c0ab4628b05e5f4812f4`

```dockerfile
```

-	Layers:
	-	`sha256:8971f97e11fcdc503f65b5e942d47a9ead2268d6003bcde1c3e46b9243e9bc24`  
		Last Modified: Tue, 16 Sep 2025 20:11:23 GMT  
		Size: 4.9 MB (4856888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9013307606a0e891ed352374afa740b69b212109eb8e6bb7dc3b7e3faad87831`  
		Last Modified: Tue, 16 Sep 2025 20:11:24 GMT  
		Size: 40.7 KB (40727 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:03e628afa029b9fe4beb6f62c550b7051bcf938111b829fafd7d2cb50e28467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.3 MB (436341194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1cd6676b46cc1553de698c32897adb4357b2407ad1d1eef770599a854a3768`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T20:18:41.039Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.7 org.opencontainers.image.created=2025-09-10T20:18:41.039Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=7ccf3080fcbd0ec666f88b3b7515537bd70da14c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.7
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e709c4c77b969007eab14b36e65a58881c5a72a7ab04072526ca669c5f424e0`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 9.4 MB (9446078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61fba0f0254ae2a5d2b62efc9d29ecfcb3189516df1ff962224d079865d80c`  
		Last Modified: Tue, 16 Sep 2025 20:12:48 GMT  
		Size: 381.4 MB (381394042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7088a36628b2e16f045c64a3c744363cf2bdf25462367b64df6d9a3a46aa18f`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f14f8edbe2a4d1edae3796f4384929ec7d722ebb0fbbf41d3429f6a7fdf28`  
		Last Modified: Tue, 16 Sep 2025 18:02:54 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e577cb0c8cb43baa3d4c3a1b1d914e63881bbea99458d14f1d10a83415cf8e84`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132e7d441925515192f217a9a07d7cb242dddf23495f8c7c56a6ef08a9e3461`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a1240fdf15ac05b00f2626f0c2d9afc9e0bd0633616d6c6c38af26e5a52c25`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339c77bd36b5d156f2e2548a0218b88132e90c2af18cfd85c1b03b279f53934a`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff719dafa43003a675ade25a01953f6960d9ff672c028fa37a8bed174fb82d`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2523ea48c6243d4e05df4b3128fb52df2b1e6f8ca2e0e367c80f0e0549821d5`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 158.0 KB (157990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b4b3191bc8f95fdb3f66fad1ae8a0bffe2912b4a4865b1151026ed132002c0`  
		Last Modified: Tue, 16 Sep 2025 18:02:53 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.7` - unknown; unknown

```console
$ docker pull kibana@sha256:b8f2ef2c5080c60387a4da88e9d8def98c0adb1dadd6f98e8b5fc3c44b2e3feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4898926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a14363100270d082110a807242109d6642a9ed9939cc202df4fff61e1ca854`

```dockerfile
```

-	Layers:
	-	`sha256:11d76f818953c2c6e98b513fb61af780bc8bc0833d59913a95c6a2e8a4a1eed6`  
		Last Modified: Tue, 16 Sep 2025 20:11:29 GMT  
		Size: 4.9 MB (4857952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddc442e946945700b206335064d96edb131aae911aaa8556fdd93fd5c220ee5`  
		Last Modified: Tue, 16 Sep 2025 20:11:30 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.4`

```console
$ docker pull kibana@sha256:cd90e1bccac59a8bf97d4bcfdb9cb60439119e3e4a3604a8f5e9d4bae9502b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.4` - linux; amd64

```console
$ docker pull kibana@sha256:d9c60a212584ac18b10777193f08d4920f2aaca07dbf1779ac232094b10df101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436883793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552ac60c6cd69a7fc0f4481bc050fa06b4c4124e5afbc2325244148a3d6bd176`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:07:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T11:08:45.034Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T11:08:45.034Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56558de458071f5470de7ffc60ca1ffd81cae3e76d5c3565cb9bb17e528020a8`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 9.4 MB (9432027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02375930a9f8f36c8ddeaf2b8c5183204b18e487e35051d8940498ab824040`  
		Last Modified: Thu, 18 Sep 2025 19:12:18 GMT  
		Size: 381.1 MB (381084642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72c7e10b9112209bdcbc9068e5faa8a81d3142ab5879c9b10e2f5cf83f98ca7`  
		Last Modified: Thu, 18 Sep 2025 18:58:51 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1831e156f53f1195eada618d2677d60672ffe231f461f42e54827789097b4b3f`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 16.5 MB (16460481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b4493ff80b34245f3499c234cc155def038d9d9b07d37df87a859b555631d3`  
		Last Modified: Thu, 18 Sep 2025 18:58:51 GMT  
		Size: 5.2 KB (5237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b9995ea451665334bb996e798d5f2d092321533110d9f41ecf5796d977111`  
		Last Modified: Thu, 18 Sep 2025 18:58:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2015cbc9185718a3e36d413e74fbf8f6304d7c32537a936a5864b86644e4f4`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429cd00e5d4ff66068da70e11f1955dd6a95c640c3addd8227cc2d0ae50ea43`  
		Last Modified: Thu, 18 Sep 2025 18:58:53 GMT  
		Size: 4.8 KB (4801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a2c12027b21bdd9bc4a66dadef6811b4f5ff2e02e764f5619f9499a24011b5`  
		Last Modified: Thu, 18 Sep 2025 18:58:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac29a41b2a16b6bbf2b1dd33f124043eb3aa9a1b0dcbc00b317af5ac5518b56`  
		Last Modified: Thu, 18 Sep 2025 18:58:49 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b90f081a47a895990a9f9e4351e40deb0d1d3599b5435d01e838c71b7f700a4`  
		Last Modified: Thu, 18 Sep 2025 18:58:49 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.4` - unknown; unknown

```console
$ docker pull kibana@sha256:a1610ed6d6402083252aaed2497b0256e1cc1f3811b644e9708cda50a96e8a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c303da30ff32cfd74d61f6d3a3c96c558efec6a0b2904356ddc24bd57e6e7e`

```dockerfile
```

-	Layers:
	-	`sha256:41c1a1475e169bd28e1bc49be639c8cc44114e75211bced069ed34b917ac347b`  
		Last Modified: Thu, 18 Sep 2025 20:11:28 GMT  
		Size: 4.9 MB (4870464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c6ef9bafdcae76318ab1a94ecfb1e0bcaa35c371e427287b2a1fa712a5d16`  
		Last Modified: Thu, 18 Sep 2025 20:11:29 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:762366ac3bd296dfb38b4c287bb461b2fdec945fd264bbdf2923af74c07661e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448895036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09fb37e64662426e38486bf4d11cc9d72f600436a1c92ddf05328ee3025e3dd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:07:26 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:07:26 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:07:26 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:07:26 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:07:26 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:07:26 GMT
LABEL org.label-schema.build-date=2025-09-16T11:08:45.034Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.4 org.opencontainers.image.created=2025-09-16T11:08:45.034Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=57608cbf53423b24acae7c1e589faf57a6bacaf2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.4
# Thu, 18 Sep 2025 08:07:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:07:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:07:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679fcdc06f87ca1cca4651c1d104324ea77bb80b07830b0fab85ad781320b6c3`  
		Last Modified: Thu, 18 Sep 2025 19:11:31 GMT  
		Size: 9.4 MB (9446063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dc92bc77c2770c2c352932eb9bd16ee5c5585cff98b6cc505aa51ef371b3a3`  
		Last Modified: Thu, 18 Sep 2025 19:12:15 GMT  
		Size: 393.9 MB (393947864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb1019509877965322f85729856a966a189be8b1378a97a51a5a22907e14fc9`  
		Last Modified: Thu, 18 Sep 2025 19:11:24 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d423dea7b72ccfef5524c6ff8db3fdd2314e55ed3b9c54eb39414ac9c3ac8b2f`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714ca99ada151ebae3f8a96fc1ae3e177784c84d98bc14d24f31e20aad081a7`  
		Last Modified: Thu, 18 Sep 2025 19:11:24 GMT  
		Size: 5.2 KB (5237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fae890ce61e2a0c5880adc6abbd83d46aab1052354c620e417571186e552402`  
		Last Modified: Thu, 18 Sep 2025 19:11:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b694ac47fb2ab2bae2d978bbb6e274c89d4e743e426d4afdd3ff03cc45c4250a`  
		Last Modified: Thu, 18 Sep 2025 19:11:26 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04469ed4c141d92d4576392d7a8fbc3f223bda6acf2f92611e173e806c7c17a`  
		Last Modified: Thu, 18 Sep 2025 19:11:28 GMT  
		Size: 4.8 KB (4803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8957caa0bf7e61e21d8b8c665295cd8b406ea70dd29b194ab51456c5c5d883a2`  
		Last Modified: Thu, 18 Sep 2025 19:11:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c08bf5718705e1c9e783e6df5e280d68ef0e5978f7101f06b68752d5ca52c0c`  
		Last Modified: Thu, 18 Sep 2025 19:11:27 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b034cd1a1ccb9396b273eafc4a86d2fd87392bc798b7b5b0b638a5a2ab6c647`  
		Last Modified: Thu, 18 Sep 2025 19:11:24 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.4` - unknown; unknown

```console
$ docker pull kibana@sha256:c3db42fcbf70b12e5661353d4506cd720be9fbe858e5cb9d97991ebd4dc04039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4912727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5be31ca524045f4ee861de7477c3cefd384f71e42c7420d7eb251e67f0ca97`

```dockerfile
```

-	Layers:
	-	`sha256:e6a4b9227f437c43ef8b22ba5c6b0ee1d901321e31cdc8175d856f39c3d39f60`  
		Last Modified: Thu, 18 Sep 2025 20:11:34 GMT  
		Size: 4.9 MB (4871528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb1e5dfcb9b8a9ba621d094292ecfbd57963bad9b029d5301ffc1fab0f5545a`  
		Last Modified: Thu, 18 Sep 2025 20:11:35 GMT  
		Size: 41.2 KB (41199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.7`

```console
$ docker pull kibana@sha256:930f104056a8f4bd438a92c4316ab1d2abe112a0ef2767babdaa59e30fe1062e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.7` - linux; amd64

```console
$ docker pull kibana@sha256:3ff178bf235e23fcdc68af380d0f97b226ddde2a26094d26a93c1a3c5f2f93a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438659210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7ad69373d9ad1e9236a264dc0f3b89f1b7ec9c7f0ee0e53a16fdbec511184d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:33:24.878Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:33:24.878Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abce95227cd9fba95832429448370785492df3e779e53a6af848090351b68f98`  
		Last Modified: Tue, 16 Sep 2025 19:10:45 GMT  
		Size: 19.5 MB (19528358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd46ea2c771303137ef3bb44948e81f5e33bb689680877ca5f41e158da8e787`  
		Last Modified: Tue, 16 Sep 2025 19:11:19 GMT  
		Size: 362.9 MB (362924817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51067c241eba0c3b71761e023d1d78b6be09e8b3064e1371dc697fc46d446255`  
		Last Modified: Tue, 16 Sep 2025 18:16:27 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0f795d5814118a5ab0b2384e28e922b38b68dc1a43c56f8c9f7ccaa6705015`  
		Last Modified: Tue, 16 Sep 2025 19:10:41 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a4e7e9d1067fa9d693c66c4a940734a1355cf3a1bf6da60f35cdeeb4a60d0`  
		Last Modified: Tue, 16 Sep 2025 18:17:19 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64c8257fae8479c67fa7e9ea480a2d1147e4a912f9c015658b65b8960e54765`  
		Last Modified: Tue, 16 Sep 2025 18:17:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ccf7daa361e1345c5362a0891f89f3d7623dded37073b52e61b0f8af05d85f`  
		Last Modified: Tue, 16 Sep 2025 18:17:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4b858f28d2a3d7d54ad746b7c46e32b497d657b5ba99adcfc95b0338bced53`  
		Last Modified: Tue, 16 Sep 2025 18:17:31 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e12120861d309eb30a6264d80efe4a04bc3dfe53d9375d213a3d8a5e15c2fd`  
		Last Modified: Tue, 16 Sep 2025 18:17:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3efb053639c29b74a65e86d543f4bd42c40ad159243e28d681a99c1a13ee5ca`  
		Last Modified: Tue, 16 Sep 2025 18:17:36 GMT  
		Size: 75.1 KB (75098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9a9e55c1a2ee0de82ad152dbe5718da45c832f2d3d71ed61a45471bfe8ed9`  
		Last Modified: Tue, 16 Sep 2025 18:17:39 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63e33b0a29219d1014a8fabf70db4ce9b2531a4ea7da8b96cbf40f33a2c8a67`  
		Last Modified: Tue, 16 Sep 2025 18:17:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.7` - unknown; unknown

```console
$ docker pull kibana@sha256:e163f72ed10904e828bf27a540242f7c053fafdffdf53adba4a61834fe5d38e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caeec167dca90fc0aa85f7743aa78197fa286b46803731e617114d9ba383e9b`

```dockerfile
```

-	Layers:
	-	`sha256:e899a7ff0c7d67c92ecf4e0696a219c4fc180b30e0bc585636d3eb10fc035797`  
		Last Modified: Tue, 16 Sep 2025 20:11:36 GMT  
		Size: 5.6 MB (5566575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c7abbd72cc350dc85c366418fc0472c53eec68e1e6283062b10b29f29d482b`  
		Last Modified: Tue, 16 Sep 2025 20:11:37 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:57602ab87dae9c489f5251336f33578144bb5e32f082f967b6bd2ff5aa98dc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.0 MB (449952780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9b7aab627ee287abb0155fadbf177f188c6b23417a74366e37f9ae440a995f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 16 Sep 2025 08:32:12 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 16 Sep 2025 08:32:12 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN fc-cache -v # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
WORKDIR /usr/share/kibana
# Tue, 16 Sep 2025 08:32:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 16 Sep 2025 08:32:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 08:32:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL org.label-schema.build-date=2025-09-10T22:33:24.878Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.7 org.opencontainers.image.created=2025-09-10T22:33:24.878Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=9d44cc2d50d27f4d3ae7b72f0fe6b612508674bb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.7
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 16 Sep 2025 08:32:12 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 16 Sep 2025 08:32:12 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 16 Sep 2025 08:32:12 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32939d187c84ede7ad26af3238073e066bd5a4cefbca98229224a92e917f4191`  
		Last Modified: Tue, 16 Sep 2025 18:01:48 GMT  
		Size: 19.5 MB (19486535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c55d988e623eba7aa952472348004acdbd764d743ac7ce04211707a368b4a6`  
		Last Modified: Tue, 16 Sep 2025 18:10:43 GMT  
		Size: 376.0 MB (376049456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c4128c8dcb8c5d8fa0df5d78e4ae17fc4f303fe3ee0c429001a16acec995e`  
		Last Modified: Tue, 16 Sep 2025 18:01:50 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa8fa0a33c7061b1e5e689df0db0cb1c55ced27a7e9bdfaf1d25e44bf3fe28e`  
		Last Modified: Tue, 16 Sep 2025 18:01:48 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94637488a332e0c826729f49cf66f152265b6201638c8c0e4cf82b956b157ca8`  
		Last Modified: Tue, 16 Sep 2025 18:01:47 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83896f35e05c9858f4b13f1d98a653ef1ef4eb2fb9d0e38a4178c604311275`  
		Last Modified: Tue, 16 Sep 2025 18:01:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468dfe4dfb47bfc3f5a88ee8d1d060b31974734454f8e528735d5018bb69b24c`  
		Last Modified: Tue, 16 Sep 2025 18:01:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87c1f15290ed241bc8f8c498a3b2a9777abe6db5528ace9012bab720271da81`  
		Last Modified: Tue, 16 Sep 2025 18:01:48 GMT  
		Size: 4.7 KB (4692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d8eb6e7849869427060aa641d2354374c3a11ea62dc04cf07d192348b3612`  
		Last Modified: Tue, 16 Sep 2025 18:01:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f4d52b62238b40999ab5f94016be7ac6cc5fc59a6ebf16463c1b1bf225b388`  
		Last Modified: Tue, 16 Sep 2025 18:01:48 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e2fb284167154692990b2bc73e008aa3cf83cd477a9c0fe60ee906648526a`  
		Last Modified: Tue, 16 Sep 2025 18:01:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8bf26a4c985a7de1e3f0eb6e6e9625d2acdfa5b492bb1a918df5a41bb9600e`  
		Last Modified: Tue, 16 Sep 2025 18:01:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.7` - unknown; unknown

```console
$ docker pull kibana@sha256:649f1b7771e9d9665ae925e50950dd1e998127dda4286f374188e4ca0be40ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6029b13670453496e3ab4fee761b6697f078355ec71e932279cec8fc6abf3497`

```dockerfile
```

-	Layers:
	-	`sha256:4c78606490a392a97360bf620d2207ba261f49786f3eb87d2d5dce3c18aaae3c`  
		Last Modified: Tue, 16 Sep 2025 20:11:43 GMT  
		Size: 5.6 MB (5565253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a4d6cf6ac227189f5d07fa49599c9d347546cfb0e9c7b742aa582ab16afa80`  
		Last Modified: Tue, 16 Sep 2025 20:11:44 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.4`

```console
$ docker pull kibana@sha256:64ab9a927f9da7f6b5a83580f068c7b63add9c8f6cf475e4930662782e20c4e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.4` - linux; amd64

```console
$ docker pull kibana@sha256:bf8742c6ca8fbc968499ed3f1df81da533952aa0577a2bed03d31a7694b3afa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437874934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09a73ac392bc5e35c56c5865c5efdfa7029baee1619d3db055aeb88961fa7cb`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T20:31:52.531Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a8042692500503cca8f3d4aed3c38da398c22f9d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T20:31:52.531Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a8042692500503cca8f3d4aed3c38da398c22f9d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f48667cb34e05f88ae51aad7d578fb082ec8a0e7343f588eb5f03236ca8642a`  
		Last Modified: Thu, 18 Sep 2025 18:59:09 GMT  
		Size: 19.5 MB (19528353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a620ad19ee1a2aa3617a1e3986aab77a4b31cd599c93fad156d08016e00b1a89`  
		Last Modified: Thu, 18 Sep 2025 20:17:12 GMT  
		Size: 362.1 MB (362140503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6046c0334f1bc9bbc49a3e136cb518d8c95f761803c8248c281c5dfc4c65cfbf`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250f92560144332886792919585d5ffdef8f8ffc5829afb8c1fb938093e9612a`  
		Last Modified: Thu, 18 Sep 2025 18:59:09 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3361d0cafcbd7f6e87fa857e5511c7c8aea354923d7ba2f23465b07f4c625cb9`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c50f93c0d7e97afbe8ab79556ae547a4653a45be91e155531fa68d7d8f85a9`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17c3218904a591d1ee27db593b1aba65299b30f0e6d4c342a87f6df9fd4610e`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e059b65069160b6d0eb28fb86aa90461e2d5b1f7ef5a94609032d0978f92b98`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 4.7 KB (4726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696354901066ea610de241dd452521d5d0d09ad24fcba39eeb0ac1c60e29e01a`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5acc54f3b6bc76981aacd34316c5cd320bbd1daf222eee8875b00ba334005c`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bc89a453078fa3a1dddbf58290d8b72f0648d4931d87846d170d5aff72f080`  
		Last Modified: Thu, 18 Sep 2025 18:59:08 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c173a89bb6fc94602375320e6a701ebf38c21fd4c1fc97dd83b08bb3e6a0470`  
		Last Modified: Thu, 18 Sep 2025 18:59:10 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.4` - unknown; unknown

```console
$ docker pull kibana@sha256:c346275aa139e11dea832dbcecd0b37d2067e1be14531e5b8a12f800e0d78695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a83350eae7821a0c1d163a19768ebc985906dc9af685dfe3367b05a69bdfb6a`

```dockerfile
```

-	Layers:
	-	`sha256:6065e9995dfe2eb138c702f140621b1355fbe82b34193bf2ac1545bf06be3e46`  
		Last Modified: Thu, 18 Sep 2025 20:11:39 GMT  
		Size: 5.7 MB (5691260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a19e70df8018501007990fba168c6d9b30690a5c49fed65941b0466b7b9f083`  
		Last Modified: Thu, 18 Sep 2025 20:11:40 GMT  
		Size: 43.2 KB (43184 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:225994b191ed93ffc81e4b56d2f87b05289c5f06995cec25bb8ebc1ac1c26516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448895386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02c080224df9904dd1d97c121076b7b0dca96949a4ca69df601402f93c272b2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Thu, 18 Sep 2025 08:05:18 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 18 Sep 2025 08:05:18 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN fc-cache -v # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
WORKDIR /usr/share/kibana
# Thu, 18 Sep 2025 08:05:18 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Sep 2025 08:05:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Sep 2025 08:05:18 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL org.label-schema.build-date=2025-09-16T20:31:52.531Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=a8042692500503cca8f3d4aed3c38da398c22f9d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.4 org.opencontainers.image.created=2025-09-16T20:31:52.531Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=a8042692500503cca8f3d4aed3c38da398c22f9d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.4
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.4 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 18 Sep 2025 08:05:18 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 18 Sep 2025 08:05:18 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 18 Sep 2025 08:05:18 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051822f7a7fdbe61316e3684576abc588d152d6a0281b85b78e1cb9fb8038278`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 19.5 MB (19486497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68077f76d34303c9a743bd0137c4a6d94ff6ec74361ff15a3bd901c4a19adc01`  
		Last Modified: Thu, 18 Sep 2025 20:16:40 GMT  
		Size: 375.0 MB (374992088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b1b731b99a9aea7e10351c2eeb503e72d04c8e1eba440344b7381c7a4f1a85`  
		Last Modified: Thu, 18 Sep 2025 18:58:19 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe83540d8084223d178f11e525527b4e82a6373e361b338cd663361e26c6f02`  
		Last Modified: Thu, 18 Sep 2025 18:58:29 GMT  
		Size: 16.5 MB (16460479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfe66da3f1c75d93479589f1cadcb0bfc72c75ed395e8894491b6562a14d055`  
		Last Modified: Thu, 18 Sep 2025 18:58:20 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aa23d464801bb38235d57be410fd797d8c5b5b2a6c0669d8d3d07f12d90b93`  
		Last Modified: Thu, 18 Sep 2025 18:58:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea829c4cc5b960bc204921c5608099f4c8d3078b85d8814cb7f230c1fd156bd`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95ee873c77c9467c15e5f139eade2cc25ab7d7c36098c23be1bb5716d9b1373`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f750a9171695979ec6f2b0132638fda2c010bdbc4f57e0ee334a1bb8afe39ddc`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023018b9e613bbd0f81b5ba6092d354ec2ac749672ac95e4c33b7e143165d349`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 74.0 KB (73985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42afa7198ebcfe3ab0b0f0d1158d680c9fbe312664452a37fc899b3dfb23824`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ee51a6de5dc60f0ebf51867e5edb98e05d2561c62d167601ae102183964e1`  
		Last Modified: Thu, 18 Sep 2025 18:58:21 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.4` - unknown; unknown

```console
$ docker pull kibana@sha256:f25c2bacac7bba85e3923f0d20d4dada208a37c9d7c0683413be6287650ebf73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd0b39e967b05d032c55ed8d150bffae538937bff813571b430ccdc4f9f98bb`

```dockerfile
```

-	Layers:
	-	`sha256:81a735cbab62389040e2073687b5b367a491903d7dbda57c297f041718c3d219`  
		Last Modified: Thu, 18 Sep 2025 20:11:46 GMT  
		Size: 5.7 MB (5689938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293f0f3ae65f19109c4e2c0a853b939813b38d0b02c9e2e54dd7cce1defce478`  
		Last Modified: Thu, 18 Sep 2025 20:11:47 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
