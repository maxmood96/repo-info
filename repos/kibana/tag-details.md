<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.6`](#kibana8186)
-	[`kibana:8.19.3`](#kibana8193)
-	[`kibana:9.0.6`](#kibana906)
-	[`kibana:9.1.3`](#kibana913)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:85c128dfec2c3933b7c18000b28f915d2e809fefc08cbd8e9675e46099aebd20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:93a05ff9136e38f0f39e41ebf437562cd02343dc9b15757ab07f5191d76fd5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353911017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7680dc6a3011aef284630f6f9060a4aba6f0c6c86b8d42d6858a4f573c6d0b`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51230c45091a12df86d5e8628d68f815e6bc9dfa66f222440195c69d3ec14229`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 9.4 MB (9431862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8021ed2684e321da45dbb5db24ab16a732b15a8f9c235f8b557dc9b0f872c4c8`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c21f509b2e348e536bf6df286b06275ee35853dc2aab1cf14c719036dc9e53`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60429a247d383196ec1f7f1de3f4c2705630c1b35b3b1622ede409a0d36a39a8`  
		Last Modified: Tue, 02 Sep 2025 00:30:18 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1535ff005d0c5a7457dddbf6b18ff14532e1333dda4e19786116e2451be8ce59`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4519322c62f5be2911a15a81c10b6d25e26b2243dd415ec85beb28d118d3bf9`  
		Last Modified: Tue, 02 Sep 2025 02:13:57 GMT  
		Size: 298.1 MB (298112497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9616306d70d2015e8198297c2950e727113bdaf8af176b735f90c502e786`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776e559f0a8ac75b7c79e87ab99ab7c8f6d0e5f1894c4e5b97157986a4bf5631`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23521436e303cff387d635b5a2333d56c283adf60a3ca9eab6a87de3505444`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056871ad96eeeb58ac2436caf172840cfc7ead46420b73714edd886de148bdf9`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c3196dae94abd2168a257d97fb98ef26847e281d88f2eff42cc4089b0c334`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04993a920960e5c000564772ce039e747dbb9fe107b6dcf02918e71aac53046d`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:78abca99355a47ad2788f0c6fa6a96d0221c4f052970e0d0e180f179b381e957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1619969ea7f7dd8744581dc50f432aa21452f4d5a2c7e8edf67c136699b232d7`

```dockerfile
```

-	Layers:
	-	`sha256:5bb37931117743cae8b7308fc8c6585a5b96fbd40b75a1f324b58e312a7ddb49`  
		Last Modified: Tue, 02 Sep 2025 02:11:18 GMT  
		Size: 3.5 MB (3506830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cba3f68b9fe90817b1bd9f33affa6040e501ccc26945d3540167c596444ebb`  
		Last Modified: Tue, 02 Sep 2025 02:11:19 GMT  
		Size: 44.6 KB (44554 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8e4cff4a10141f1e39dda53afe4af661625f368487425213632ef6543ab10b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.1 MB (366093818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263b0cfcdca9e4da22f13da0d64db0fc9a2d2e9cd141e579ab4b28f524c7543c`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3d7ab8b3b037decce432e2353971e48b71d33d0e7021b290c34e2d4afd6a8b`  
		Last Modified: Tue, 02 Sep 2025 01:54:43 GMT  
		Size: 9.4 MB (9445783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caab08fc1bcf9aeafd5d592dc65cb63789607c800293eb2932884392a5194fdc`  
		Last Modified: Tue, 02 Sep 2025 01:54:41 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409888f54eb6ef40b16e77163577668d6c1c01b3c34b2e1ba9e24b51eb108ccf`  
		Last Modified: Tue, 02 Sep 2025 01:54:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb223be8d0c6be2a7e0afab2695cd4849b0fab2e2c19c9a777a515c074d72afc`  
		Last Modified: Tue, 02 Sep 2025 01:54:44 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7acdc9e63c8e51c87664f121c3998be68bcb123559647a3ba3b60f7eef823`  
		Last Modified: Tue, 02 Sep 2025 01:54:42 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45ae5672f8021facc200c8279b9bfe43b87c20e0982f5ab2f0832c9406e7ce2`  
		Last Modified: Tue, 02 Sep 2025 05:15:33 GMT  
		Size: 311.1 MB (311148085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2687d24f0a1dc4f69f2c99d7b5aa9278a12de1e6e48ae949c2bbc991ad5552`  
		Last Modified: Tue, 02 Sep 2025 01:54:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587b0f66db6f6fdd1cffceee0eb272c25f47d917ca06d3d29380ef50c1d6ed53`  
		Last Modified: Tue, 02 Sep 2025 01:54:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbda1503d229441f4d63a3a3ab9b9ecd1a62941516f200d35e4e1ed3c9a2cd4`  
		Last Modified: Tue, 02 Sep 2025 01:54:43 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eda373c4d0601fe89c6173cdc612c8fca9a590343f526d140b14079d257bde`  
		Last Modified: Tue, 02 Sep 2025 01:54:40 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3c24b49e0a674bdc526c6449daadbc1d6a994779aaad5a9e67e30c7351a179`  
		Last Modified: Tue, 02 Sep 2025 01:54:39 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437c05ff46719ed7f619b5d7645f22117679834fa970da9436bd04214ad4bf6`  
		Last Modified: Tue, 02 Sep 2025 01:54:40 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:916d696020ff7d959501a0fa50976502138f2817d9d24da9de04b187dd46136b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7805f66c3be00ee5ef40b22cc54f6e05f4b59ad3be475138e64c5bb73124d451`

```dockerfile
```

-	Layers:
	-	`sha256:afb878e444cd7edd6d8c3bc7bc204979b4964766abc605661a764570f192181f`  
		Last Modified: Tue, 02 Sep 2025 05:11:20 GMT  
		Size: 3.5 MB (3507894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0923e6e5c6b0812997456b144da717e6cbbf429315eb3d7ba6f185d982a6496e`  
		Last Modified: Tue, 02 Sep 2025 05:11:21 GMT  
		Size: 44.8 KB (44832 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.10`

```console
$ docker pull kibana@sha256:e89c25896500afe57af782cf1d6d56efe1ed8eb2399de0a03daef9f5a368a5f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:76e225a6fb855cfc84697d25479fe2f62d8d59022169eb18d1f162131906b2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403301151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66eea01510671f794da8ded4dcb1a5804876e9d56e6c78e2b142f4492118732`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b295d945e78c2eec382a63b6c2f1b543315ee5630fa05d4e74debd2ae0854`  
		Last Modified: Tue, 02 Sep 2025 01:45:11 GMT  
		Size: 9.4 MB (9431813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a790d368a9b54f45b81c8ad107997fe77c057775715d0127a11f929618f3027d`  
		Last Modified: Tue, 02 Sep 2025 02:16:06 GMT  
		Size: 347.5 MB (347502642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b8581cd2b7629f4472a5cc61dfc7fec08927e2190d1d2ee1ae7084b667a920`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde7799eb7587c3f2c2f3db86a3b528180f8f7bafd5f80ef32062b10eef6082d`  
		Last Modified: Mon, 01 Sep 2025 23:40:57 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef96d16cfda78456f389f37caa55a16d91ec41ea711b4e5dcb56970e6c73b085`  
		Last Modified: Mon, 01 Sep 2025 23:40:57 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc941c7905aebd7542c5ddd05194c6e69bbe80d5d4d38a745e32c1e9495052`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5d3efa714cafd32377ff36e5d432fddac75e1743d3ec697e7b4875e51f10d4`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3041bbfe4b92c73466bd75e4652816b3acf1432e81d925e0caeb6fbd9cc565d9`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 4.7 KB (4730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1c025878e3d66f16b052601b68e2b5e87e08541b513ec74de6c7d40b7640a3`  
		Last Modified: Mon, 01 Sep 2025 23:40:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16340f28589c78931c4441720efb0bb578c1760c7a33a00f8fe707720dc5d7b`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97b4decfd2b9f96a89fb57e8dc0b5d955edf7cca5624f868fb71364b43af1a6`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:8ff3fa6dc9a1c04885c46fb316790d28846b8a2fad43e4aa19c3a1d7da01ff4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963529b5e7827ce8223520bdcc7ffe471d109c855c59f68bf96b764b2730eeeb`

```dockerfile
```

-	Layers:
	-	`sha256:f46ee49ba8f3f456c84ec98ca549b2a38eff49eebfe51d5294c7273777661e84`  
		Last Modified: Tue, 02 Sep 2025 02:11:24 GMT  
		Size: 4.5 MB (4520136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac778db419d5f09f2268fc7ecf1a368ac45b10a88ff31b79c22b803cd776c85b`  
		Last Modified: Tue, 02 Sep 2025 02:11:25 GMT  
		Size: 40.7 KB (40733 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4295665be96a54f706becd30904215cbc2e1238ea68726ae688a7f4927e37958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415497490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ff9ae955224034088bdb4352b345339eb1050a37ed52f8ac6a01fc9848410b`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad4b538f41dda355bfc54a8a9201b6ba9cec445ec4c2cbcb102eb94297a663`  
		Last Modified: Tue, 02 Sep 2025 02:00:57 GMT  
		Size: 9.4 MB (9445846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba54d334633d64cf7cb4ba6214041ac412da08d3f7e989549a751a393680325`  
		Last Modified: Tue, 02 Sep 2025 02:17:27 GMT  
		Size: 360.6 MB (360551670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9963e7e93b09897d5a0c413c54bee31dba9065eb505e0dc54fa2b6d217f46681`  
		Last Modified: Tue, 02 Sep 2025 02:00:56 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c930de0eb6378f84425f93a90ddbf7f956c30cadae1df925ba186ea5aee5be`  
		Last Modified: Tue, 02 Sep 2025 02:00:57 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561305581cd87b47d26abedb3d921a0c0c9b20384471e079255440faa98c3354`  
		Last Modified: Tue, 02 Sep 2025 02:00:56 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45785cfee148c0e6d9ed92354930882131b3424de1a31d435db999e3fc02356c`  
		Last Modified: Tue, 02 Sep 2025 02:00:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49784038a866c3a2fd80c883c73720209c4558126b4bfba07f08f65a0fe39306`  
		Last Modified: Tue, 02 Sep 2025 02:00:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e9a7178bf92993412969b81a2a893f7351ad29d5308d3d595b1d347ee3871a`  
		Last Modified: Tue, 02 Sep 2025 02:00:56 GMT  
		Size: 4.7 KB (4730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91595badd6b19362eb0311a36d26cba196c643c1e24703296ad78d885e25a09`  
		Last Modified: Tue, 02 Sep 2025 02:00:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e4d12659cec0e34ebd8fd91d7ef97f03c33f6e137da1e178047338d4bbeba`  
		Last Modified: Tue, 02 Sep 2025 02:00:57 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a671a707d15f2d60f6fbfe6f59bf1281a2039ea777b7c7cc01860b695913b009`  
		Last Modified: Tue, 02 Sep 2025 02:00:57 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:b9d6de68f8b9a88cce77bdcba77ab16dba65635090ce1290e0842f13b4bb5c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4562182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f53feedbd2366887d81119ec6d71a6641100987525a6cb51269be475a6670c`

```dockerfile
```

-	Layers:
	-	`sha256:f482c093a7e8e4bfcbfde2cdd45aa5904107c87c284184a720e9705f9ab1c221`  
		Last Modified: Tue, 02 Sep 2025 05:11:27 GMT  
		Size: 4.5 MB (4521200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4019dc549eb171212978b564c98c250a91676481fcc9fe108afbea8da468a9d`  
		Last Modified: Tue, 02 Sep 2025 05:11:28 GMT  
		Size: 41.0 KB (40982 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.6`

```console
$ docker pull kibana@sha256:ea426db488a03934b9bef616b1c28a9a764d2c53d6eed75296ac7d084b025b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.6` - linux; amd64

```console
$ docker pull kibana@sha256:c02e74bc6249597f3f679cc74817b4130d6b8a9bdb8ef0ee2d9ab0df6e32183a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422897769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd44807f9f1afb1297bb099a8b1b89c3375fe50d7052e193810647213d9c39a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 28 Aug 2025 08:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.build-date=2025-08-25T20:23:12.522Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=062e5bafa439548979be1f8302e2b04e103670e2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.6 org.opencontainers.image.created=2025-08-25T20:23:12.522Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=062e5bafa439548979be1f8302e2b04e103670e2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.6
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9a35a7bacc026ac70cf10921880e4556790ed3ccb6fb89e870d5a87a78b307`  
		Last Modified: Tue, 02 Sep 2025 17:29:47 GMT  
		Size: 9.4 MB (9431833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e9d6cb81c57b5a3c992ffd34e0cc9ced35caaeb392589bbe4226c59cffe361`  
		Last Modified: Tue, 02 Sep 2025 18:46:29 GMT  
		Size: 367.1 MB (367099208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f824a00dac71df5371bb4b05c634f1889e9d64268d3cf1824aa5d9dd8f97ad80`  
		Last Modified: Tue, 02 Sep 2025 17:29:46 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d020ec4efe4afd689fd0f40251bab33c9edadbe7a38b1455aa2e58140ce87644`  
		Last Modified: Tue, 02 Sep 2025 17:29:55 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77778f53dd1bcee789ba66325f10f091dc90142a7e1b873e003527dc7b3a3c83`  
		Last Modified: Tue, 02 Sep 2025 17:29:41 GMT  
		Size: 5.2 KB (5245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0c41b5b482d26df56a44d71e42d5d34ec4a26a437c7f89513dc2d897932949`  
		Last Modified: Tue, 02 Sep 2025 17:29:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe989f95f7455b13d4bd7a5def95e306e5ccb700f1d14eda2dd9411dcff955`  
		Last Modified: Tue, 02 Sep 2025 17:29:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3f7d998ac55566665a2a7f0d78299fe2dda6f9353752581e181131fb704820`  
		Last Modified: Tue, 02 Sep 2025 17:29:42 GMT  
		Size: 4.8 KB (4763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6d286dc7e56866b45305c35c45791fe08cf6554760d72f0222d3efce4f9d1f`  
		Last Modified: Tue, 02 Sep 2025 17:29:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b04b76fe364ec33eb937ad26e160cd3987a9e50f3a918fa4483a02f122a81c4`  
		Last Modified: Tue, 02 Sep 2025 17:29:42 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242ecb501feae02aa1097766ca6546243ca9ea6b0e7c952ae080b32f0fcdfe77`  
		Last Modified: Tue, 02 Sep 2025 17:29:42 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.6` - unknown; unknown

```console
$ docker pull kibana@sha256:25262cf2c461c3c5c8713a47bb0a372f3d872845fff1bc293a9d1ed2b3393f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4905056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09f44938f9da7939fc06aebeebee1d6e7faa81935440ea5a3bededd1848d911`

```dockerfile
```

-	Layers:
	-	`sha256:cbff781f92970d99f6e0e401855c5af1136e46c52745ecd9ece9f4fb08dd4a2c`  
		Last Modified: Tue, 02 Sep 2025 20:11:27 GMT  
		Size: 4.9 MB (4864331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25b35b168cae5ddf929f60605e8d561fd60cba1a0c00209040fb254750448d92`  
		Last Modified: Tue, 02 Sep 2025 20:11:28 GMT  
		Size: 40.7 KB (40725 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9e0a3a5c29f09dc62b398b63d0dd49d5c41621209cf1b6113f52603b5f6a1c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.1 MB (435101173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c794cbe80dc59918bd8deefda85ba4afa267776ec4aa24aa444771fc4611d11e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 28 Aug 2025 08:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.build-date=2025-08-25T20:23:12.522Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=062e5bafa439548979be1f8302e2b04e103670e2 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.6 org.opencontainers.image.created=2025-08-25T20:23:12.522Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=062e5bafa439548979be1f8302e2b04e103670e2 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.6
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad4b538f41dda355bfc54a8a9201b6ba9cec445ec4c2cbcb102eb94297a663`  
		Last Modified: Tue, 02 Sep 2025 02:00:57 GMT  
		Size: 9.4 MB (9445846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc73219db70bce9013176b67b4220dcf5d4f51d132e2c5d3d1fa153a19db68`  
		Last Modified: Tue, 02 Sep 2025 20:15:31 GMT  
		Size: 380.2 MB (380155326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee881026b56d839caac1467ee5dd2d1ca8da9081b28c01d649701e2e4e7c31f3`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6ce7562626c91a8320135e18d767a954bb541579b9d93b7f6d761cb0596313`  
		Last Modified: Tue, 02 Sep 2025 17:51:42 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1ed61c29a8de6cebdf19b1c8f8d3435fab4e4f893457f9731f83038c0a953d`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 5.2 KB (5243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8442e1c328471f4413b7b7293534f4b1a1009118737c341e9ee1ff6a3bf75769`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089526657cdd57b3d1e5b9b0b9e7cc3e8047707fc15d30883c07ea0e071b95f5`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328c0f7dd597eb4d845e276345583959ad4088d180d1167deb911bbf5e905db8`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 4.8 KB (4763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effb9d31d23d77aa5b95c59b29f3aef155e2a29730645b886757d44f9bb9f0c2`  
		Last Modified: Tue, 02 Sep 2025 17:51:41 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ee096bc0de3c9e034b00c821e4b3f6d4652eb38993ef557ff1719ca8b0483f`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478d699df3b7603d41ef4261b19cc47caf4c840519c8870be35f333264a0cf07`  
		Last Modified: Tue, 02 Sep 2025 17:51:39 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.6` - unknown; unknown

```console
$ docker pull kibana@sha256:85961a161904f81c82221e92a1feb808c4bda55d31fe7ff0a7ca99453b763ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4906369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8f63ca3f96a5aad1c3b002a499d23c3e524a36ccb531846b69061dc194dc93`

```dockerfile
```

-	Layers:
	-	`sha256:f172fe1b335c6f3119a51ba5567e11e36ebc8e6c7353f84e0512e01739f26e89`  
		Last Modified: Tue, 02 Sep 2025 20:11:33 GMT  
		Size: 4.9 MB (4865395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cabfb9c28f4061fb87e944fd9694343f6c1504cf79a6b845eebbf0f661d7e6`  
		Last Modified: Tue, 02 Sep 2025 20:11:34 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.3`

```console
$ docker pull kibana@sha256:5c4ca83040260f0490b7edbb5a1ceca581bee1d036cdde48784a2302e2aa0e65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.3` - linux; amd64

```console
$ docker pull kibana@sha256:7f7a1edc744e1d38a031989dba700ac049b87dbf13d77f4fbc8d64bf0761f64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.2 MB (436158276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc4007c1cb7cb52e4ae3ebedfc89a1ebac3ef1d3b47b58565ae46af37561835`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7fead9f7a63d788f3e25781b3bc8862cbacf199e0a4580f9208c582cd7940c`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 9.4 MB (9431869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422295a559973fd7f320c199996e314eb8bdba2b0fda3de15bd2ec28885adeff`  
		Last Modified: Tue, 02 Sep 2025 20:17:17 GMT  
		Size: 380.4 MB (380359643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e10557dec99eb6859c110c21bd26b9729cee8acb0400490971988e5a7369be4`  
		Last Modified: Tue, 02 Sep 2025 17:29:49 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037c65ff24befa1e216db6293f83428732d7afe0f56ccb7e720a0e442401dc1b`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3e1411d6816c94866195cc8d92bb1f67ace33402a67e803a6559d599c86dd5`  
		Last Modified: Tue, 02 Sep 2025 17:29:47 GMT  
		Size: 5.2 KB (5238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c494d9fb19f6c1fd8b75402449db389637f5a50ff6c250a0e1efdc6038615d`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe8f1740ed61d675e9a9e3bb1b537e0b7069b54f704c8b34a728919f88cc86d`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607979bd03ff1ea20a173fa1bf5ad24c2a31c253bfeba5f3e2f5f7d4a3acb0be`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 4.8 KB (4802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548a077edc8cf625cc2087032f836f16fe88f4d66b98b385b67e8c6a95e891b2`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5844cb56d4bdf5862b6c5917d4c32609cd4c641df4d58ebd47a43a0406a7796`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747ec1454efb073ddfdce6188b3f0e02fb2d6546619c498eef1689c94bad5465`  
		Last Modified: Tue, 02 Sep 2025 17:29:48 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.3` - unknown; unknown

```console
$ docker pull kibana@sha256:51e9b8a6d35115a0a4575af846e189de471c4a3cc76405a13afb8605d99a6e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4919937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628e600c00068414f6cfa28b87cee50ae81a5254631535af081ab8b145879394`

```dockerfile
```

-	Layers:
	-	`sha256:0f9d47a6e1c4568cbde468fbba35e701771ff4c2e62224486fa3ed8e2958a3af`  
		Last Modified: Tue, 02 Sep 2025 20:11:36 GMT  
		Size: 4.9 MB (4878986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554cfb179b029dd884898f031d15fac2c3b44770bb05da46ebab7e1d947d81a2`  
		Last Modified: Tue, 02 Sep 2025 20:11:38 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.3` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:360a4c3a2e2e6bfb105f8114c27e8f5d3bd48961ab8c64e201aef5d5cff54419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.2 MB (448179475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab6beefd912b24c2bf671eee08ee0e51c0dc90435343d05aaf6ec421d42ee7f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef38fbfa61a637e2978f5a9bce98427f2177f121f038de57710444025e9e71e`  
		Last Modified: Tue, 02 Sep 2025 02:14:53 GMT  
		Size: 9.4 MB (9445784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b306d98ba69aa506fb3950b537e934726363b407200dc02d3220ee4dcbc7e4`  
		Last Modified: Tue, 02 Sep 2025 18:44:39 GMT  
		Size: 393.2 MB (393233642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81689a5c710b81cc57bb9ced8950c5ec5ee5b42d9fc07d0f4b019cd31774b4e7`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805c2312bdf1faed014f41e19390cf0e68fb0efe08191467977cb6a4779f8d1`  
		Last Modified: Tue, 02 Sep 2025 17:58:53 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6392c48c02e24928a4eddfb67c9b230f1e6b3fe37af908d3746a4d863110277b`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d84157fc777225d3b8a78f1b2a780d5e6c96261f3f9d056e0106f7e96e5893b`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7202c30d3af8130b99bbd676f3157c34738fccf15d86717520bcd7175f1c57`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ade7ef181ae602c3e0624a3bc168520f858d193838ed09e25e3095b344057`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 4.8 KB (4806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6f096896aa1cef3619fcc58467687933432dd61f4e7dfc97c7e7b5b1e407a`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d920f11b6bb670aa922c1a4ec0a2649a28cd3ded672bb3f5c222a72c052fea1`  
		Last Modified: Tue, 02 Sep 2025 17:58:51 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675357f8df560f4e07e7877de0268a25d3b945c69c91efdb8e9e13cab3f54d1a`  
		Last Modified: Tue, 02 Sep 2025 17:58:50 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.3` - unknown; unknown

```console
$ docker pull kibana@sha256:e613cd80e00b22416fc1157f6656c0d8bcd782ead856c4e27ed4a2a7bf919acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4921249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b27aa6c0aab6e2dcb90355205a4f0006d150974bb182b9934e6a87578a5c9c`

```dockerfile
```

-	Layers:
	-	`sha256:2719e9de3f0dda08bfb50d216aa6c1384310acafe7d37f2b1cf05f2731fc43d8`  
		Last Modified: Tue, 02 Sep 2025 20:11:44 GMT  
		Size: 4.9 MB (4880050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c971bfacb20bab45bcf91974c34e5fb3b768230c7c32076247d0c0783461ad3`  
		Last Modified: Tue, 02 Sep 2025 20:11:45 GMT  
		Size: 41.2 KB (41199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.6`

```console
$ docker pull kibana@sha256:e9c8164386c13b62ce2000eb67d8b8ddc1286282b5f4b2fa243e35c137fd67d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.6` - linux; amd64

```console
$ docker pull kibana@sha256:782ecc2bd1a8abe636f814f78b4bb41189ea5bab62c9641235f248d61531913d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437346896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabd8334c6c9f5ad78ef5eafbc1fcd895d5bc3d9155f27eb58125879582bfddb`
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
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Sep 2025 11:31:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-24T11:25:39.092Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=042db7248f4083cb1659298cf6a84625b71fbf58 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-24T11:25:39.092Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=042db7248f4083cb1659298cf6a84625b71fbf58 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Sep 2025 11:31:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Sep 2025 11:31:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ba0e4e493da8c20cff0fe2db8a3bd106857420f4d596bbd994a7ae3816fc66`  
		Last Modified: Tue, 02 Sep 2025 17:28:48 GMT  
		Size: 19.4 MB (19375911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81112b18c79438b7cefa1dbb742536972efd35f9f334c95491f48e400cb59cc`  
		Last Modified: Tue, 02 Sep 2025 20:23:18 GMT  
		Size: 361.8 MB (361764955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5399ab04f6bbf9b3502e7914f7ea5788f3470c70b353bbc18dc0c9258e24660`  
		Last Modified: Tue, 02 Sep 2025 17:28:46 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9368f0ae63334f51bbddeb634133cc0ec0b0af0711663e0204b1cde39b59886b`  
		Last Modified: Tue, 02 Sep 2025 17:28:49 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec068470ea832e9a1c984a8e2e44f68e26edc79e9ea30c7c94567b21e2db6bb4`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdcf058a48c804bd3b60b0e08585231fefcc9e3d8c7ea56bffe571de18c2860`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00528ee1cd576bb24cb2c61def119f35fb90b01b65c69b646f6dc36ae952a1`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a34468027db0cba7c81c6a14112dc421483f053fe86e3b4c862919e502654c`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 4.7 KB (4691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c573a95463e38bbeb9d46140d4410b65165bdad6dc59e8b12b13821b158d361b`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abe2480987da2e35dab00deb2cb2f187756ab0b310ff963383c7776fcda5be6`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 75.1 KB (75099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134dd3e87a38b661ce43f593eb6857ba6b83a315854d3eb3c605eb42085cfcc3`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0948383a1e9febbce990f67cf09e625a1d07a1a05b5b4ebe263e9e3cbc76ac0e`  
		Last Modified: Tue, 02 Sep 2025 17:28:47 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.6` - unknown; unknown

```console
$ docker pull kibana@sha256:25f84176568ef4ae9c9bb349911e8c591425a95bf5a22bcdc3b0ed9bd113fa9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a273fc13a257d2cc82a5737a798c2ee895332caca05c311a89a2f0f0c17aa124`

```dockerfile
```

-	Layers:
	-	`sha256:cf661605d8cb29ba8d8f1380ee28362fdd1b3b2250be0fc2b6f33c039e8517f6`  
		Last Modified: Tue, 02 Sep 2025 20:11:46 GMT  
		Size: 5.6 MB (5574036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d732fe3aca608621e177ad08eb3c66ec9111ded9fda0b24c40f76bf0f6a350b7`  
		Last Modified: Tue, 02 Sep 2025 20:11:48 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9e516585c1d4de6e1d7d7cdcfc94b5fab985e2915127bac78474e54b96969317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.5 MB (448532661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4ebd304edd3e59d43f44587b93dc64ae8de2cbd3d923c4963a95062f268ff3`
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
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN fc-cache -v # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/kibana
# Tue, 02 Sep 2025 11:31:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-24T11:25:39.092Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=042db7248f4083cb1659298cf6a84625b71fbf58 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-24T11:25:39.092Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=042db7248f4083cb1659298cf6a84625b71fbf58 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 02 Sep 2025 11:31:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 02 Sep 2025 11:31:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 02 Sep 2025 11:31:20 GMT
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
	-	`sha256:f123169d2da31f739b88d1c4f2a7a971bc49b72aad743b61f465f8ac0f533c9e`  
		Last Modified: Tue, 02 Sep 2025 20:22:08 GMT  
		Size: 374.8 MB (374802548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c832aa7eea50dccab200f0312be7285cf6ad6d6c309db001c673ae9d1fedbbe`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc6f4937f9f7fba51f2aa6c71f0b5d12f54ad9babc017e89f814a34354afab9`  
		Last Modified: Tue, 02 Sep 2025 18:06:02 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc805cbd14cfb392e15205550697a5a69225f62d25f45a68673e142d60d027d7`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3c41e9d353ed414096ea87a1df07148adc164ba726062339fb34a28c3d701`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d064e11226d4e82cffa92127de4c6310342c2759e353f8b140a849d8b10679ad`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08548e633e810ac5ad88df5095e4ed1080c9bc7acf9b8495414532da50a9318c`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 4.7 KB (4686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb36e6a6cf2a0c2fceabd4479921dd8f25c2e4d7fc8ac194dd4dc07066b0b87`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cc89e8098bca9fd3af8c73ae1a3142891a1af20a4f5108b091e0d04a6ef078`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09fda6af369722a8d5f993844f871728311b15a014e7408483eda42dda2f30d`  
		Last Modified: Tue, 02 Sep 2025 18:06:01 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b487ed957dcdcd6f215ae22866c6aacb32537a74ac3b60ffdf56e17d04da2df`  
		Last Modified: Tue, 02 Sep 2025 18:06:02 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.6` - unknown; unknown

```console
$ docker pull kibana@sha256:76e54732b449395147ecc645b912194f2ae898eb51a31488e9fbcc45441204c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f362f2873c7329a1fc5cd14905b32302c8fff39699bc7350363c034875680bbb`

```dockerfile
```

-	Layers:
	-	`sha256:deee6192c0d3520d9ca2bb017c4d6751a87204953b5a724a1512a35876d04d8e`  
		Last Modified: Tue, 02 Sep 2025 20:11:54 GMT  
		Size: 5.6 MB (5572714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d760fedb213cbc9acd410d0793887c14cc6e9dbaf2da6f0bee870190083ac9db`  
		Last Modified: Tue, 02 Sep 2025 20:11:55 GMT  
		Size: 43.4 KB (43440 bytes)  
		MIME: application/vnd.in-toto+json

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
