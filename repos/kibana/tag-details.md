<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.7`](#kibana8187)
-	[`kibana:8.19.3`](#kibana8193)
-	[`kibana:9.0.7`](#kibana907)
-	[`kibana:9.1.3`](#kibana913)

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

**does not exist** (yet?)

## `kibana:8.19.3`

```console
$ docker pull kibana@sha256:05ce34149448dcf59905025d224ca43a978b8777b353274a352acc269b9fc32c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.3` - linux; amd64

```console
$ docker pull kibana@sha256:4c9f7adc07b8d4d1b02ec9f62339d61db0291ee67fe191c81b55af4f7662ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.2 MB (436158702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be19fda7222bfd99488268fca5467c3f0f30dc891f89ae1f44b44681add5d4a4`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:19 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:19 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN fc-cache -v # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/kibana
# Thu, 28 Aug 2025 08:37:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.build-date=2025-08-26T02:13:22.134Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db23d2c570cbead7fcc72e6a60e33ef6af8e9ff3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.3 org.opencontainers.image.created=2025-08-26T02:13:22.134Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db23d2c570cbead7fcc72e6a60e33ef6af8e9ff3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.3
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e706335c9ec7ae795acdd7b426ab7903ec94086f686d2312ea0b8a8ba4790f`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 9.4 MB (9431993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59544a69028e051151b040ff28f808d2e1e6a484f2cfe375d533fb9ef72a4a6`  
		Last Modified: Mon, 15 Sep 2025 23:19:08 GMT  
		Size: 380.4 MB (380359565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41caa2b95eda65c7bd7f32d4c575fd5e9074312cc41f473167549b4075fef795`  
		Last Modified: Mon, 15 Sep 2025 22:28:34 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2b7021c70e9074bf80f95f875595809079f70b0a16e6a14752d1341280d50f`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a346b972aed37a8a6919291bc3100f3be5cfc9a68206a9cec199e5b63b65bfc7`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2df87e288a8406d14adb97cfc458737972971ecaa5c6f0b585c8445e8691e40`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8033b874c6f04cd3b3b31ea60798a42a2b7fe737e9bc63673ccbfec18fa9a0c`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a872960bde54c8b04c3f24adf3799ac2e015e6f25edd73dede33de11be12b`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 4.8 KB (4802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb0a416fa8f120f38a187ac168ea5348a789fe7a3768b94f9cae43e339b7839`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71357c967ec8ba7322ddc31fef65484d9f6b38474654de057cf64dda42082564`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 161.5 KB (161452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ed925c009363704631ede730a9105947bfcdcbbf7ac96a527341a94f200f01`  
		Last Modified: Mon, 15 Sep 2025 22:28:35 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.3` - unknown; unknown

```console
$ docker pull kibana@sha256:a3c635de4b20b659c948269f1784faee47e172407f2ce37209ce29d6a67d2174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4919941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686f8699d9e36a34a336284d222f5310ce695fd9459e66b42bd7e8a288a183f1`

```dockerfile
```

-	Layers:
	-	`sha256:1191cac15603285bbd097ddedf62bedfe7c6c4d2a55f5505bda3ba915246d292`  
		Last Modified: Tue, 16 Sep 2025 02:11:52 GMT  
		Size: 4.9 MB (4878990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68df71430afb44a65c7f0b65579f5ed731a63a20882b8af566ac20a4aad49f7`  
		Last Modified: Tue, 16 Sep 2025 02:11:53 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:ee7e5a140a08a0657f69fc107826443a564c1b74726583a60e885f588cbb18fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.2 MB (448180683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6f23a8e3d6618ab74273752e9152b63acf51993c1637ae4ad445d83c772eb9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 28 Aug 2025 08:37:19 GMT
ARG RELEASE
# Thu, 28 Aug 2025 08:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 28 Aug 2025 08:37:19 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN fc-cache -v # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/kibana
# Thu, 28 Aug 2025 08:37:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.build-date=2025-08-26T02:13:22.134Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=db23d2c570cbead7fcc72e6a60e33ef6af8e9ff3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.3 org.opencontainers.image.created=2025-08-26T02:13:22.134Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=db23d2c570cbead7fcc72e6a60e33ef6af8e9ff3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.3
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70901749d45176be6e5d4309225c76aab1b0aaeb6111891abe4c5f518b3da704`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 9.4 MB (9446069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c037fd99dd2391060e03cedf454e270a0932c9eb4aadf6aae3583ddd56e2840d`  
		Last Modified: Tue, 16 Sep 2025 02:18:09 GMT  
		Size: 393.2 MB (393233509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c783229e897c940cb8bce22c7202ddacd37d8f8d4a5cf05d763cc5f9529b0c2d`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a19eea0000a999c53517553b8ebba8f38744a4f06a5130879358409ba363d9`  
		Last Modified: Mon, 15 Sep 2025 22:26:35 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1204958615e5f3cdd3d6940c96c437129fec8590fea144e70ccd67bf9184e212`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e0b0f7512ba01c2eb1a2dd2b697500b475dcdd4cff6b83404cbe7b1dec94dd`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abef8250496de8055c287b8f5608234c221ecb4305297be408f135d5a265d27c`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f4acf2a5e23a433a63d8d8408135a903e71a070fd976d14827e355e9e9b90e`  
		Last Modified: Mon, 15 Sep 2025 22:26:34 GMT  
		Size: 4.8 KB (4800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5ec27bce70928dcc6b2871ac4f19e098bf3ce06dec53d24c2f4b5102bcbf9`  
		Last Modified: Mon, 15 Sep 2025 22:26:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0703a7d3fed600b3650031017c403179d96d0d1c3adcb19d2c03789f51675`  
		Last Modified: Mon, 15 Sep 2025 22:26:35 GMT  
		Size: 158.0 KB (157990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf8c634da4263501e2dbaf0f8a85d8e2c7002d90a7e46d9afa3a28550bc55e1`  
		Last Modified: Mon, 15 Sep 2025 22:26:35 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.3` - unknown; unknown

```console
$ docker pull kibana@sha256:913e7a751e2ac089c0aca2aacb574a4c4d9846c1c5516ea4aa10137be3dc68d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4921252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723e0f99432e48c757788a1d165f11e993b088226b8867c8d0351a5041c1353d`

```dockerfile
```

-	Layers:
	-	`sha256:a621d37da92d0b8c48cb5ab6d11c0d2ed72e8b0a55f5e30d354b6b9fdf711858`  
		Last Modified: Tue, 16 Sep 2025 02:11:59 GMT  
		Size: 4.9 MB (4880054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b7174740e63b6a3da50c1101da97f044f7b5e24b697ea24d1c941af9e93f82`  
		Last Modified: Tue, 16 Sep 2025 02:12:00 GMT  
		Size: 41.2 KB (41198 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.7`

**does not exist** (yet?)

## `kibana:9.1.3`

```console
$ docker pull kibana@sha256:13cb6730a8d671e5f80833909bcd0a081015c8ae077e2c7f71d5d02f604e4e17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.3` - linux; amd64

```console
$ docker pull kibana@sha256:09eceb5bc08ed4a01798ba6652f6b4e43f25cd317bbe410141c69e41a9304f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.8 MB (435770404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918105763743e48975828d54592044bc7d5148111a5750cbca4652de4b3a5d36`
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
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Sep 2025 11:31:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-24T11:24:41.098Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=7c4882bd34f27e726bd4c662e4536e7deb9113fc org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-24T11:24:41.098Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=7c4882bd34f27e726bd4c662e4536e7deb9113fc org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Sep 2025 11:31:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Sep 2025 11:31:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05115ee1ced6c184644746f8ddd9beab2c5f56dcc7258581b81b088178aa66fc`  
		Last Modified: Tue, 02 Sep 2025 17:28:46 GMT  
		Size: 19.4 MB (19375694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe7f4d18a3be7b615df7ecc4f16aa96cef01dd2a3d120a08e7955216a3d01ac`  
		Last Modified: Tue, 02 Sep 2025 20:23:31 GMT  
		Size: 360.2 MB (360188637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708148859d22e0cb86da67769bf9a2341dbd2db98e84ed205f395985ec07c892`  
		Last Modified: Tue, 02 Sep 2025 17:28:45 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbac498a2f7c8013f48e77a35c134e571b2d1ee944c09544b625e6768bd9c20`  
		Last Modified: Tue, 02 Sep 2025 17:28:55 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2b37eb56646b48da2074a624bde74410ba77e88c4220e5120f790e7754b820`  
		Last Modified: Tue, 02 Sep 2025 17:28:45 GMT  
		Size: 5.2 KB (5232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f37107015137036de103d623925de32aad2d3316a883ce1305f4e5de4ad7976`  
		Last Modified: Tue, 02 Sep 2025 17:28:45 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98bd5804e9dc1afce131cc9071b903bb9dbfda5987aa9171d886492058aa061`  
		Last Modified: Tue, 02 Sep 2025 17:28:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608062ba6c599a8338b741d758d2e4a51139e1b0de8b671993a3fd21f3c4e625`  
		Last Modified: Tue, 02 Sep 2025 17:28:45 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f53035dccbf9c9504d453c80d3942e985f196a2d0c54d7023249b25cf8d679b`  
		Last Modified: Tue, 02 Sep 2025 17:28:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f8c4e0e3d4cce623451b5c0d4eda3819ddf1d12ac70782025206642e36db64`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 75.1 KB (75098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca27da6aa876505e45ab96e73fe7b757952bbd24426de0d996f3750b405a5bdf`  
		Last Modified: Tue, 02 Sep 2025 17:28:48 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a029a8499c661503dc6d49985f2be4d00327ebae887177c44a6b0d5b12afd1e`  
		Last Modified: Tue, 02 Sep 2025 17:28:48 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.3` - unknown; unknown

```console
$ docker pull kibana@sha256:6073aa91f1b84f098794236dca41f3d002d91dac9e4b7b189ba8df56a65b8fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5726481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc501be86082e5789d87184586aa9ae36f7fc45e490f23ec277c0d5bedfedb9`

```dockerfile
```

-	Layers:
	-	`sha256:6a16ebfafb12400da1017e3b53a2dade58ea88c229a1b9543b6d53351148d1df`  
		Last Modified: Tue, 02 Sep 2025 20:11:54 GMT  
		Size: 5.7 MB (5683296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bf9c6fe370f2c75868982b834a624341946391653b029749f785ed6a9fa7ec`  
		Last Modified: Tue, 02 Sep 2025 20:11:55 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2c0dfdc9ce5e4dd16976b83beedb2ffecc92857cbdf30457ebf5142ea030d6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.8 MB (446786990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a930c918e80365f2639af5c58cbf62341c5a7b0bf7fd0abfc8c4ee66bd224b38`
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
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Sep 2025 11:31:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-24T11:24:41.098Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=7c4882bd34f27e726bd4c662e4536e7deb9113fc org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-24T11:24:41.098Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=7c4882bd34f27e726bd4c662e4536e7deb9113fc org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.3 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Sep 2025 11:31:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Sep 2025 11:31:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71851054ff6efe6436fdc488cacd53faab7bf1045c3a188baa24e7ae9e777655`  
		Last Modified: Tue, 02 Sep 2025 18:06:02 GMT  
		Size: 19.3 MB (19313345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689ce06ee7dd90eaecd515f795af67b38d90321d2c96db9e6f5bd5b6b3c32422`  
		Last Modified: Tue, 02 Sep 2025 19:21:51 GMT  
		Size: 373.1 MB (373056837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785dbde781bb99f8f6d853ba87889fa9f7110a371f13a956a652bcc879193fc6`  
		Last Modified: Tue, 02 Sep 2025 18:13:43 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a5934c254c9784b668d2fb3a75a5a079f74a1b0f1960bb0f3eb336d7463d65`  
		Last Modified: Tue, 02 Sep 2025 18:13:41 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ad40276374ad075c90a3ce7c562dc3a98d63f89eed8b2ed1ee3f8a9383d03e`  
		Last Modified: Tue, 02 Sep 2025 18:13:39 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23d6e6f1f1f36a64c3a1c0bb226ef214991823ce0bd2f03d68cc4f02d343bd2`  
		Last Modified: Tue, 02 Sep 2025 18:13:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45dc1c3f4323517b7fd426943b90af59756380dadfcd6059f9b93228899a1cd`  
		Last Modified: Tue, 02 Sep 2025 18:13:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db83a673e230fa81ed47af94a6b061c989ec664310413e5a6c880cc39cb5057`  
		Last Modified: Tue, 02 Sep 2025 18:13:39 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8865f1ce39c49101fb1e9e117a3389bf50c8b3a786c9c23692535131d1d04b`  
		Last Modified: Tue, 02 Sep 2025 18:13:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd7d87fe9de76a2375381ad69aa0253e6b7524785ebe78ce0d259d6c283dbb0`  
		Last Modified: Tue, 02 Sep 2025 18:13:40 GMT  
		Size: 74.0 KB (73983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6a9133faa680d627586c1fd56b3ab9c11bf4b78308caed811a5360c4d0696`  
		Last Modified: Tue, 02 Sep 2025 18:13:39 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e487a1254d0c45cb6d372cd703fd4d6911d918d65c3eb6b2005b4416d97cea9`  
		Last Modified: Tue, 02 Sep 2025 18:13:40 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.3` - unknown; unknown

```console
$ docker pull kibana@sha256:8c7407f873574ebda7b510a6d6dda986b31760232cb5ec14cce60e3595f48268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5725416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1190c9b200b91e2c2c8a6c391d81d6fb4700d002f4eff5cc10435709e243d7`

```dockerfile
```

-	Layers:
	-	`sha256:06204645e49e2a22ae91ab9626f646931a78693d7eaee2ca0db84bda382b1af9`  
		Last Modified: Tue, 02 Sep 2025 20:12:01 GMT  
		Size: 5.7 MB (5681974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5287f10bdf97973c6d2b92fd656b5db2fbd931908e1658f8cdb3cb349a7e6e43`  
		Last Modified: Tue, 02 Sep 2025 20:12:01 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
