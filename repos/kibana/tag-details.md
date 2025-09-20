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
$ docker pull kibana@sha256:c267abf7954ea5f61ada8cc764f6a5082bab1b3002e70d8d1a07d24b56e3e4a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.7` - linux; amd64

```console
$ docker pull kibana@sha256:6dceccbc2908a08df5036cb8ab7567ea7c8abb94fa9944dcb397dc9e86a37e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438662196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9679cfe731b8caea2db3a4defd3b5927d97fda819a1d5162853bbff5ee5b65`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
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
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4045a7a37d35a23951d5589e4f0758bd42083ec1bb80bbf128998a5711cbbeac`  
		Last Modified: Fri, 19 Sep 2025 20:53:54 GMT  
		Size: 19.5 MB (19530274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd752e4b644407a830db203f480a3bc1d384937739ba12b4ab13418aa56c0361`  
		Last Modified: Fri, 19 Sep 2025 23:16:08 GMT  
		Size: 362.9 MB (362924919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997a9ce9ab8f18746010dfc100cd809fb347ed2ef3c81c12e3245dd642f64c2e`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eddedb85e411d5886be217eca2a16a18c513dc951d04b6e37668f95d49891b`  
		Last Modified: Fri, 19 Sep 2025 20:53:51 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac969651755e8349243a76041b75eaf7e0254abe5b10a34ceed27930dce8f64`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bd72eaf096663a7542de1a8993aaabd5f2425d93165d37678dfb9768f3cb87`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c894183b4676744f5803cabeafc8fd275888d28bcbe0eaa5080783ea071984f`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e394a10fd9adceefebd6935b8ddd200562ae9b7687df6dc20111b3c8f47443`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e061ed588ae8c28494415a18ddd8194491c405d1060584eb32cc827236ba9797`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ab082fccb15d09740db5549bc49364b4bcce34e5a748bff68174b698cb1071`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e4114c35fca4c8b491d5b293f62bbb7da9aeff6affa919455f95e8c0889747`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b976c6f712c0b6f4bd51cd00003feeaa19b7f8108e99562b5e9e40ce70a362b`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.7` - unknown; unknown

```console
$ docker pull kibana@sha256:60418d0642ada29dac26e027e0948b0eba2e9510a84105d6278fc4bbddc04389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bbe7b10c1ff807688b1c29141f64da11252f06876a5db88e32e6efe2b3e363`

```dockerfile
```

-	Layers:
	-	`sha256:77ccf1c6c2788427ba243729bcc845d49279078de5c02c06173b28ce9cf07a71`  
		Last Modified: Fri, 19 Sep 2025 23:11:24 GMT  
		Size: 5.6 MB (5566583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab64c71b9b4d821b88ac12b4020a375b38ae71ed67b378672c722b7744d77d0`  
		Last Modified: Fri, 19 Sep 2025 23:11:25 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5391acd93cbcbeea5e628bfc874e2477315721011a5383d53b13f8833f17dd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.0 MB (449994645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ff636f1c4cea49bdf50fef357ef1e4d8fc8f0d64bcb28895ee1924794a46a0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.expose-services=""
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 16 Sep 2025 08:32:12 GMT
ENV container oci
# Tue, 16 Sep 2025 08:32:12 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 16 Sep 2025 08:32:12 GMT
CMD ["/bin/bash"]
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 16 Sep 2025 08:32:12 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Tue, 16 Sep 2025 08:32:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
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
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921f39323e53460d96daddd522f5ba7f35101b6a79c265382af520b9f77dc89b`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 19.5 MB (19487810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4834af2e5ce115722da8c6d1184c9d724d5b47bbdb6299a2ebc6bb839396b`  
		Last Modified: Fri, 19 Sep 2025 23:16:36 GMT  
		Size: 376.0 MB (376049478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4931bb7e34c8d20899ec049001cbdd5d34195271b0a07c1f27fe69b9302c2ad7`  
		Last Modified: Fri, 19 Sep 2025 20:52:51 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb225a03bce36b046b98ec21896983aa1ebec9ca34f62669d13a53b35b777ca`  
		Last Modified: Fri, 19 Sep 2025 20:52:54 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae42f40d4330079979aa91001035601784a681b696b209bc8ada08458df2cc2`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bca199880cad2c8058cfc03b5851cb7df7a43e22151c2922a16c2a35100d7d`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8defc75851724d091da013b146d55acb2f0f2997b7d39b5c0e2e46719f75718f`  
		Last Modified: Fri, 19 Sep 2025 20:52:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0cd6b8c96c716ac8dfbb0e3ffcb3146fc8b0c9c75bac16adf50563bd7060b6`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 4.7 KB (4691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b5439a2c657cb628e13a8d8eee57c78a8f67e9afbacac42837c8927deefc49`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8981afb0360d08a801c352522b4601f9eba07727e0732d9a7e1b58b6c596cc36`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 74.0 KB (73987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b640f297618711952e3207ab265ffd9ce264a355aa9adae435a6ce9c6648db00`  
		Last Modified: Fri, 19 Sep 2025 20:52:54 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c26019901bbb2f8867abd0e9f22bbbe59d3ab75e1492177ac7bc9293f2d845`  
		Last Modified: Fri, 19 Sep 2025 20:52:53 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.7` - unknown; unknown

```console
$ docker pull kibana@sha256:d8073da44f1e21fb6867e4aedfc0c7b7627d3a4b913c536ea95dfdd9290f15cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ae099cace36665211dc4a3b9b1ac44cecaa38a344380d8fe4ff424dd10b1ef`

```dockerfile
```

-	Layers:
	-	`sha256:242cbbe79e87860933c9bb5fcfb736221068ef7516103375a616c65a0bff5b7d`  
		Last Modified: Fri, 19 Sep 2025 23:11:31 GMT  
		Size: 5.6 MB (5565261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ebd2ff10af81950a8250c96d60743f83b328ff21a62048b9d1e19632cedbf3`  
		Last Modified: Fri, 19 Sep 2025 23:11:32 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.4`

```console
$ docker pull kibana@sha256:fbe8c7f43ba1cee3f130dfa490a13ec08e71d2b377d68dcdf282f1b184040081
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.4` - linux; amd64

```console
$ docker pull kibana@sha256:2870efd85d9203d93ff6b91914f09efe15e7f1f24c27122cebfc72383b2cea94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437877853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc25709ad108497bd4917c2d4fec885544eee3c3bef64f4f9946ea7b082eb9bf`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
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
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0ff6900d59320a5cdf5aa764b7da4b2ea1990d0f64c7230be5ff4e3f87d437`  
		Last Modified: Fri, 19 Sep 2025 20:54:51 GMT  
		Size: 19.5 MB (19530353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dc327c2a5211614aa9091ed08d60f98ee71750a43e6c2cea27d1f644f21ef7`  
		Last Modified: Fri, 19 Sep 2025 21:19:10 GMT  
		Size: 362.1 MB (362140480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41041c4ebf53c7b76f9a416fabece6dad42508d0f639935f318bbbb904d67952`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800b8c70fc0eec6e7a8693bb307c7ff9739612148e6b875b03b4aaf3acd45a71`  
		Last Modified: Fri, 19 Sep 2025 20:54:50 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c36b58541aad7e782fefefc43c743b0091ea855fa7ab1fa947b33170f88696`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c31fdce81bb9bd5495f91fa8562744eb736ac1ccb6d13dd4f3f53d573948336`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bf88aab3e1db77321563080e836f63ae0d954e8c00f83f3b7ee045c97316c2`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc80f0ee980d7d77761ba94182f29c70581dd796dd7152e10bce3c55a7472f10`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c436622930db43b9713a4c474d18e069a4e361d5150fb431a5c58948ffc4c44`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9048c5fbd2af451487278284eae789e0b6be95ae9039a25a304cd505dac9a3`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 75.1 KB (75098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fb8ceebc71b5a5c14119f24678d999d7d04029435dca5eb059d72f5be01b87`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9b712b970f7d02d3d190e59146520adbb256c348332780e2e16d29203a8944`  
		Last Modified: Fri, 19 Sep 2025 20:54:49 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.4` - unknown; unknown

```console
$ docker pull kibana@sha256:84c98b97ceddb63431c85c5cef98997903012487ece3df0c9d5237e67d53a603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f259605cf67576a65c6faad5c28b58ae90622e7518e813c4273182624d71a1ba`

```dockerfile
```

-	Layers:
	-	`sha256:ad8c37540abfb6292f6769309aaea4f31b85d46db469763c96dae1b99bbfbba6`  
		Last Modified: Fri, 19 Sep 2025 23:11:36 GMT  
		Size: 5.7 MB (5691268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee73b0ffe77ad49b494587bb0743bf77422e695d4fbe8e5ffaaeb74b359ad7cf`  
		Last Modified: Fri, 19 Sep 2025 23:11:37 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.4` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:81ddc03c9779701495eb7118d0ea044719e5fa0696e3fa570997f24cb4d8d388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448937255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ec1ea077a9894a7465e1e647794efb0b80bae351a10d1e3ffa2b379bc2a30b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:05:18 GMT
ENV container oci
# Thu, 18 Sep 2025 08:05:18 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:05:18 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:05:18 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:05:18 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
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
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a589fe1b7484b7b32fda76842867b3e22820d68f901e497aaea69d50b4b21e`  
		Last Modified: Fri, 19 Sep 2025 21:17:59 GMT  
		Size: 19.5 MB (19487762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e624f6982b55cdd460e22b285ab90754b442355f29d36fe72166db258000f7b`  
		Last Modified: Fri, 19 Sep 2025 21:18:33 GMT  
		Size: 375.0 MB (374992105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8919afed3fee77a0155aa1acd61669813ba3e2c9d78daea54813f2aa3a3d9da9`  
		Last Modified: Fri, 19 Sep 2025 21:17:42 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210d968107f3bd2e238cae0bb384c980a65ee2f175982f2078501304a32af3e9`  
		Last Modified: Fri, 19 Sep 2025 21:17:58 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574d6700e05245cf5628ce7449063c71660df7ea64b09bc11fe0ec25b957bc94`  
		Last Modified: Fri, 19 Sep 2025 21:17:44 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b88ba7f76e2d163bdde6d9992baa26c0589161e379da0aecc4fc4791433bed`  
		Last Modified: Fri, 19 Sep 2025 21:17:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69e188feb9bc73f49a8f504af4a73e22e05419e4f2ae82be9af753b2ac7fad7`  
		Last Modified: Fri, 19 Sep 2025 21:17:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276a76e8a3b98363927f4aa814ba24eb55d2fb637b34398b8ad81b6c164e6cb`  
		Last Modified: Fri, 19 Sep 2025 21:17:44 GMT  
		Size: 4.7 KB (4724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce391345a5657cbafcb553dd940465c53d169fbfdc1674ee60dd8168c23e0e9`  
		Last Modified: Fri, 19 Sep 2025 21:17:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef55f0c7e2f1da713de38fd4e67ca4965741b85636fa2c1c5d6a216a2c068847`  
		Last Modified: Fri, 19 Sep 2025 21:17:46 GMT  
		Size: 74.0 KB (73987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2c822f4b0405e69ae5a87e2639bdc900c1adcf52e132690ca889d02aa937c3`  
		Last Modified: Fri, 19 Sep 2025 21:17:42 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26e44288cb442407b2d828264c629552333083dbb05452b2e9a8d9b58fd50d1`  
		Last Modified: Fri, 19 Sep 2025 20:53:50 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.4` - unknown; unknown

```console
$ docker pull kibana@sha256:fb207c39b8232427df1789a7735a8017f2d98bbd8d6ae7a1c00b941e9a16b421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899019ccfff28e86740d5a0de95e23f1c9f72ee189b650d8e550f6df1a934a7a`

```dockerfile
```

-	Layers:
	-	`sha256:73b07c0f58bb8fb4d38f355277258d558e3e9f91940a6fd4f8ee4f4863d7fa8e`  
		Last Modified: Fri, 19 Sep 2025 23:11:45 GMT  
		Size: 5.7 MB (5689946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de59e3c3b1c78be42ffcbff18ffc5de545e705655d0df21eaadbfcf7b129e94b`  
		Last Modified: Fri, 19 Sep 2025 23:11:46 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
