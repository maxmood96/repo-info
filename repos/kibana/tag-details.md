<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.5`](#kibana8185)
-	[`kibana:8.19.2`](#kibana8192)
-	[`kibana:9.0.5`](#kibana905)
-	[`kibana:9.1.2`](#kibana912)

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

## `kibana:8.18.5`

```console
$ docker pull kibana@sha256:e1befb7d80bfc6980224658d1fa42833302f54a24832d02ac2e1c881ef6447b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.5` - linux; amd64

```console
$ docker pull kibana@sha256:ea30a3f7caec07f02a32dea79279c0942b661e8cfb7bfd52ed0b8b9b1b2a28b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423316189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f784b3936c1eaf395229df7d59894e20ed27ac6b0797995662af4ecfb1edc7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T20:16:41.306Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1ac33f19e9d91983b71ac580abe325579e2d7495 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T20:16:41.306Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1ac33f19e9d91983b71ac580abe325579e2d7495 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cd026036ebc02ac6a9fb8da345501b3cc6e2fe0a6502527a6246bcd492f868`  
		Last Modified: Mon, 01 Sep 2025 23:13:43 GMT  
		Size: 9.4 MB (9431891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdfb344ece88b9674bc68ff5c965e4d3b406878788bf710828d8d894c629fc7`  
		Last Modified: Tue, 02 Sep 2025 00:28:59 GMT  
		Size: 367.5 MB (367517578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69913c76075c640a12ed1c23c60e1a0cd8e67178215c275888c88541b3cd9f34`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6f4fef45464bd813925937a4ba40ae9c0fea5deb0a907ba859c97e8e12ebcb`  
		Last Modified: Mon, 01 Sep 2025 23:13:42 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066ccc8ebee31859379f03a36b9fcbdbe6ccde8b82eebe455ad006c06c2d40ad`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef7024990011175071370348c647d7e9a4df49004c4c4fdc13b24a8a279bd08`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6798ef3cd30483eb1cd0ff6726a506b498ea99ffc9164d835dc57752b62684`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1927a8341449024f4d9b68850a89d072d24f6afe522b2d4c4f0d05e4480fcca1`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbdfd6aa29cb6fce224fc42e51173baa20688e2a327e3b4e837347a06baa9b`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed3bfa8ea5c09135f8fdafe7171286013690a013b85ab6b1c4689290dd3161`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac243767a58834025647d3fb943bef7e51f1eed4ea02d5d6488913888c3bbac`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.5` - unknown; unknown

```console
$ docker pull kibana@sha256:eece99544ac19e0f1a61758a1ab0428b1b832117d0ba25dd7eea995117de4bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4917379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00df3421ad6058fed9f195dabb3ddb2f63a77e4a580a4731ee5170412d259b6`

```dockerfile
```

-	Layers:
	-	`sha256:4d19bd02211c8dfcb55b8f838401fb7402702560ac7a06da312e3094d7a3f3f7`  
		Last Modified: Tue, 02 Sep 2025 02:11:30 GMT  
		Size: 4.9 MB (4876652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82caee081562180c29895474e65bf8ef5ca032e68d55b64e3a0f02f88bef0c17`  
		Last Modified: Tue, 02 Sep 2025 02:11:31 GMT  
		Size: 40.7 KB (40727 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:f2a58140315c3658aec44e8fe3134f8f39b62bd3036566c17705c203dd8b4540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.5 MB (435496827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad00f6db499902bd1db956bf6abf71ddd29fe1ca0b403f219fdf988023707cc`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T20:16:41.306Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1ac33f19e9d91983b71ac580abe325579e2d7495 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T20:16:41.306Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1ac33f19e9d91983b71ac580abe325579e2d7495 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:34 GMT
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
	-	`sha256:3ec2381ab0e8cc0e90294680771ae00037257e8f07fb721a3bdf38c80673c4c1`  
		Last Modified: Tue, 02 Sep 2025 05:16:24 GMT  
		Size: 380.6 MB (380550982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc2bd4c4b8fb16c3da13a225cbf0485183bfc73632cd7a15eae90c5d06a601`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf91c6b0f7ce9d6e6b8e41a13a7d02d9059a8189c3ff22f42dc6f4f31097376`  
		Last Modified: Tue, 02 Sep 2025 02:07:49 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6fc6d7c47b8abf2a5bdbae646fdd717a965fefc96b90a46feedf6661616216`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e0e3f0d5d6f20d92fc780fd631808ec0cd3a42a0d96e2773f70e9239822c49`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8095f33f65ff78639cb4d72bce0e3c318166e612ebfbc53d907a65a34c7693ea`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ee2865f9eae4cf198b160a0e048e995fe84ac39598ec7d5799e8a59934331c`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 4.8 KB (4763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad9dac8e9added2e1897922f2bedbd7e4fd4f16205d42513dbf822c8dee6aa`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ede669583da4f9a70b729848177cd9d64ed6df3663fbe9323ebc98241270d`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 158.0 KB (157989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1b1507747afe3504e74a832b6abad99a9e43b02515165d9706e6ccd6644dad`  
		Last Modified: Tue, 02 Sep 2025 02:07:47 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.5` - unknown; unknown

```console
$ docker pull kibana@sha256:e430172504b648fab94fb7a65d60ee00cd25fd94764330053125bfc02b3c1f06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4918691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7e162f49d2bf4c80560e63467cf525167d325abc80a9f81b69a1588801d9a6`

```dockerfile
```

-	Layers:
	-	`sha256:7953768f6161efb0a3da08fbb2341097f40b93f612ddd73727fc2406204a6974`  
		Last Modified: Tue, 02 Sep 2025 05:11:31 GMT  
		Size: 4.9 MB (4877716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3249b3b117a91091478f565524ecc82b9d9dccefa5824ae768e92d8e7534721`  
		Last Modified: Tue, 02 Sep 2025 05:11:32 GMT  
		Size: 41.0 KB (40975 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.2`

```console
$ docker pull kibana@sha256:d96321b158a9a07b990597c614a057894acde4d90e84aca950b8879bf15e6201
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.2` - linux; amd64

```console
$ docker pull kibana@sha256:0852c03f3bc8ca7748180c02f014cb01b8baccf9c59b1ef6c919e60923a8133b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436104859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60c987bf3ef8d4aa37ea70e42d1ab795bda627482d714e93422bf567cbf43f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:48:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T11:07:38.658Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8634f44eaffa9f009f50401a2fbba85c95739a38 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T11:07:38.658Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8634f44eaffa9f009f50401a2fbba85c95739a38 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8f01e28d0afecec3a8a8b86d11c177f8ee2a742bebe96ea24e4bb391fbbd49`  
		Last Modified: Mon, 01 Sep 2025 23:14:41 GMT  
		Size: 9.4 MB (9431835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb99ac34b5cc6d5f160f1631df9b845a23b9d12b73d6227974ca3ad9f93788e`  
		Last Modified: Tue, 02 Sep 2025 02:16:54 GMT  
		Size: 380.3 MB (380306259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408a89f57b02a4833d291faa3e9c741869b66e11e8571e8280bcf400089ec701`  
		Last Modified: Mon, 01 Sep 2025 23:15:34 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942734dcc84fa260416003ae1587accc7c0d4de766704eabbddb73f2ba31c3f`  
		Last Modified: Mon, 01 Sep 2025 23:15:36 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3649fd817900abc6b313597d3e232005dc6cc7392e3ed45ff4f417fec76d60`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724a44fdceb618a3bd7350d2bacfc25676a2a3dd98d68ae56631afa4f6c8845`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a65c0876745c2d2fe373944355b84d1b5cf9d0034b81d42429a61c162c38538`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ec5a362b8c6355585a8f2ecf1d4a5f2def906631b03be27551ac9c7c7cd08`  
		Last Modified: Mon, 01 Sep 2025 23:15:42 GMT  
		Size: 4.8 KB (4804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576153d20c27f46a03a558dbd0270657a78a11d27ebc45b32155e726ba82075b`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8632fb15fe5b8ea4e22c3c32f2319f5997dac5a1dad68142f52c2d069b65bc47`  
		Last Modified: Mon, 01 Sep 2025 23:15:34 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4fd2cc54cc784f83b28b6ba6fc4e48931f84e7b829c3c48e5753ee2a97955a`  
		Last Modified: Mon, 01 Sep 2025 23:43:11 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.2` - unknown; unknown

```console
$ docker pull kibana@sha256:341139543d3f6447c068bac18e3d82aeb13f7f5d6daa8ae167a2462af7507f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f00a3536cec97cb5c083c5d24317f2b67cbe7de0d5e4a6678f6b8f550a4dbe`

```dockerfile
```

-	Layers:
	-	`sha256:bd8737549ea2afed6d04080dbbf1064ee81dcd43103052dbfcbb96e1941069d2`  
		Last Modified: Tue, 02 Sep 2025 02:11:36 GMT  
		Size: 4.9 MB (4891307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33c665efe3bdfa16ce047db5cf22a3254109e065b0f3f7187e411b9b11a8757`  
		Last Modified: Tue, 02 Sep 2025 02:11:37 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:877a5df5465b2f6f11d030c9a95478b33bb3909828439814e2167a07205880b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.0 MB (448035055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35341c842d42800bb89a3e1d13d965278829f4687fc915bcbea3eb4c6a82269a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:48:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T11:07:38.658Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8634f44eaffa9f009f50401a2fbba85c95739a38 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T11:07:38.658Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8634f44eaffa9f009f50401a2fbba85c95739a38 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:48:35 GMT
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
	-	`sha256:3bfcfd9bb629dd79363e1c2de8ac0e9c51e093a5d765e662e96f9b26baecc0fa`  
		Last Modified: Tue, 02 Sep 2025 05:16:58 GMT  
		Size: 393.1 MB (393089226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925afa72e9bde6fbf77c9e7a789a8b31a1252d53866512185a929a82c3013fb0`  
		Last Modified: Tue, 02 Sep 2025 02:14:52 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab138cabec2aae2cd42fd6b9d71bab693ddb0bab4da4ad8ef70fdaf84ee98060`  
		Last Modified: Tue, 02 Sep 2025 02:14:54 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d41c3cff0d87b0fbd5b04c633b47854565fa2bccabda385f6bef39e2082dfd0`  
		Last Modified: Tue, 02 Sep 2025 02:14:53 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae648766ed0da197e3720d8afd116623af2d6539f792920bb469b8b1da186a2d`  
		Last Modified: Tue, 02 Sep 2025 02:14:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a390cfccff3176af36ee0903b3ddacb1170f4333969430bb921e6ea66039ac7e`  
		Last Modified: Tue, 02 Sep 2025 02:14:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c20e7cbcb8fbd9634420ce4ebb5d3952eafae1168f0225719db3009b9d8c4`  
		Last Modified: Tue, 02 Sep 2025 02:14:53 GMT  
		Size: 4.8 KB (4799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1680fbaea09cbe0787a70145c18e8b844fd068a168385541c8e683853fbebcad`  
		Last Modified: Tue, 02 Sep 2025 02:14:54 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856091bced8938d6187a341e176a042528f547651248af6cc96445dc7ee35c3`  
		Last Modified: Tue, 02 Sep 2025 02:14:49 GMT  
		Size: 158.0 KB (157994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f485bf2cef61104948122cbaeefca75874d12e49fc8ec5bd7af6a58ad3e5b1`  
		Last Modified: Tue, 02 Sep 2025 02:14:49 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.2` - unknown; unknown

```console
$ docker pull kibana@sha256:5a309f428ce9d43dedd75f1fe85bee865b89abd7a00c972f3fb6978d83c1d94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24da96c73962fa5380b141b901af04ef6e2b477ee7a18bac05ebf59ce76c46e1`

```dockerfile
```

-	Layers:
	-	`sha256:e881d85fb534e122f9353fe275bde5790f575fec7a88d7bc346b91e0834be5ac`  
		Last Modified: Tue, 02 Sep 2025 05:11:37 GMT  
		Size: 4.9 MB (4892371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64d0178bc1a110859b4be5457154549c56bb57f407b22cb7d04b04b2c7ff755`  
		Last Modified: Tue, 02 Sep 2025 05:11:38 GMT  
		Size: 41.2 KB (41196 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.5`

```console
$ docker pull kibana@sha256:8080a59eff90e73e85f09e766dc4d7446ce2adf40148bcfce8d3dd3645a2260b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.5` - linux; amd64

```console
$ docker pull kibana@sha256:fadc76f6d509afd38d9207dc566425cecbec55f9e250390b09675adffbf40afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 MB (437757489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249525bf5c4cd277f012537e73b5b3e22a057c934dc360b54a49d272861d2e4a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T20:32:53.139Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T20:32:53.139Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e17d3f5c0b2229f3b09ef99dd1b3a631c4452b575f7c856db6bb4f4df0f76a`  
		Last Modified: Thu, 21 Aug 2025 19:12:10 GMT  
		Size: 19.4 MB (19380838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9760276c89b92f8422bc4914ee5c102c4b5912ff697298e1bba8dbde59c2966`  
		Last Modified: Thu, 21 Aug 2025 20:15:54 GMT  
		Size: 362.2 MB (362170623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26609de6a2f8a5c57ffe0fbe3b399c83e28a0567199865079f10d670d82eb069`  
		Last Modified: Thu, 21 Aug 2025 19:06:35 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30c60fedeaf8a927e3c74aeb472d5166b012038ae54a0f1e937e52c5249d4cc`  
		Last Modified: Thu, 21 Aug 2025 19:06:47 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a889c238ee3a88831f1cf18f2047025cb532fc49e2f4c2b4edccfc08a31503`  
		Last Modified: Thu, 21 Aug 2025 19:06:52 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c71c0c956bdb180bd28690c429643e04a6d98eaea524a25c98a4c08885c837`  
		Last Modified: Thu, 21 Aug 2025 19:06:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041d5433f8e43d7ffef8f3b1e3dfa63261201f492447321348ba057507da971b`  
		Last Modified: Thu, 21 Aug 2025 19:07:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8702fff66136d11f9c6b3a4b2fcafdeebd99bd789030cb937a3154421663f`  
		Last Modified: Thu, 21 Aug 2025 19:07:07 GMT  
		Size: 4.7 KB (4688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89fddae438f81ecfa789ae4a9c4014cd2043fd1bb5a3bc213aedfd74348241`  
		Last Modified: Thu, 21 Aug 2025 19:07:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff09ab5dbab955527978f0e1532e0931112ae77ccdc001560b7f11dc7383b4a`  
		Last Modified: Thu, 21 Aug 2025 19:07:13 GMT  
		Size: 75.1 KB (75095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ef8901a4e65b23bcaf085f915f638189564f542d8f48aa7ab4defe5473b9a`  
		Last Modified: Thu, 21 Aug 2025 19:07:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638623b817c9dc8f608d7da4e60c13ba740c1c2ee84aae29671c7e698d9eb395`  
		Last Modified: Thu, 21 Aug 2025 19:07:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.5` - unknown; unknown

```console
$ docker pull kibana@sha256:f589c6a50440d13cb8bc9b1136a1a389a1d8a21075cd7d4b4779343dc378bfe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2b91ebca315414bcc578af3cebf4215dd17ddb296e2adefd675c33a3250475`

```dockerfile
```

-	Layers:
	-	`sha256:ca1851ecae6fcbe58c7938875a5465068989b844ebb141f940eb11a82f966194`  
		Last Modified: Thu, 21 Aug 2025 20:11:26 GMT  
		Size: 5.6 MB (5585066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6285a7c6d58e7efb4a2dea64e087293a4462d47570831a30302ece9de67a8f9`  
		Last Modified: Thu, 21 Aug 2025 20:11:26 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6a15e2f5bd9ef49ae3badc4668c1561536ace46f3e0e7b51611f547adfccff0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.0 MB (448955462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c174a8feba8bf9a8abd41aed1f8dec11c41cce3a1816c23983bb76e366edc2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T20:32:53.139Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T20:32:53.139Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e8b56e4723ec079a70aa0cfe1546349f02500063f34e283876aa2ab251abb7`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 19.3 MB (19312287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f75167bc54122bfe8f809b1be855a00f8be7d6e84c6da30b359d9412c99d29`  
		Last Modified: Thu, 21 Aug 2025 20:15:40 GMT  
		Size: 375.2 MB (375226396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812541b37abba24a9c2e7f36d90629d3a708a946394718bad52518e086835d8`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ca81978676e38c38a25a90a5354b2731f84b9c9a5409917c15ef93a46bbec`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f760752b507d296ee12351c40dcbd449bb7ff4b34765c345b680099cf20a4`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1972d4252ba16aadef078b74f0cf37c1c71c2a0753ee16a23122e2dc24b00`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b357ee3585bc3258a717e5fb509ba0d2b80db12ea39d4110c782978fb0619cd`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0015a883b3a2490cadff00b8b257a75c75887f343d5bbef35a2159e3954bd7`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f30281d82914ac50ffc385b968ea9383297b52a5e552e688df20d763229a2`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd36b5927908c0d292cd60a205535e7b4b993f3cb6cd0b80ed3abac132523840`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 74.0 KB (73985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45a9924f107ec4dc6acda6565fc8601bc547409602782e464cfd9f349ce6bf1`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ba6dc9e874f31987d00857c793354e6ef98bfc75c0eee848a8b13dae43c525`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.5` - unknown; unknown

```console
$ docker pull kibana@sha256:e0b99ece8a532016140f0a0806cd1467b41928d4a5986fbbd91b057d91c01b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5627186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d502857bc6cc2aa1d3a2e67b01e441d4ae3aa0f260538fe40165b1158e85319`

```dockerfile
```

-	Layers:
	-	`sha256:661d52d8dc0fea4f3ca16aab2ef950072c72ddad373b8d9cdbedeb74e3a0e766`  
		Last Modified: Thu, 21 Aug 2025 20:12:30 GMT  
		Size: 5.6 MB (5583744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ddf189f68d40d4117eef0e50c75d1b6439e4c9e968aa91a192a67b4d6fc934`  
		Last Modified: Thu, 21 Aug 2025 20:12:25 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.2`

```console
$ docker pull kibana@sha256:c3aca1e84676c1aeadbc86eaa922bbe60085366a3dff3d7704f4cd70817d0800
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.2` - linux; amd64

```console
$ docker pull kibana@sha256:55280d35582bfc3f21ec395776f20c2f9c8a9ca35108792a82f2135f59aa37f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.7 MB (435699518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8207e151109cbc9e5ec951d1baea81f2cd6a9146b9702e9d27ad2610cef4c0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T16:35:56.587Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=616b79995b497dd1c83937d5f71450516b36b6fa org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T16:35:56.587Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=616b79995b497dd1c83937d5f71450516b36b6fa org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1cfebe487f50a798bf1ac93ebf4ee16c43e6af60dfb3210b7a119c279874e0`  
		Last Modified: Thu, 21 Aug 2025 19:12:05 GMT  
		Size: 19.4 MB (19380854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f308681d8a817ba4b98d90121baf52fe7be5b3da3fdee7809649c47a35d13b`  
		Last Modified: Thu, 21 Aug 2025 20:16:30 GMT  
		Size: 360.1 MB (360112605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0e44f2b29b2704fc376116d990f752fd83250c2236aad4caff04c58f8221e`  
		Last Modified: Thu, 21 Aug 2025 19:12:03 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4e103d41a0bcd7c3722b77b1c88ed73e5ca094cb022b75bf83dfb45309c014`  
		Last Modified: Thu, 21 Aug 2025 19:12:06 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddbde8bcd7c45a9fafa150263c8bb4d0189c687894fbc0105f6e6254db1e8b8`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617227c6813679eeb1859781887bed5746e38162acd69334e3fac01745a892df`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d31f789eb27330e22c9b383fab8c5e1f992fad78c91a2225238dd2dcfe20644`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f13e742bc18adc30afd1768981e33cb7140abd89605fdaacc7217342f6022a`  
		Last Modified: Thu, 21 Aug 2025 19:12:03 GMT  
		Size: 4.7 KB (4723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e607192c6b2634115924b181a5c46c85defaa40a5a61fcf42c9d78040d10a799`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d580e0f83fb9d274f0fa1e392d28489ab7cbace71e6eb71264f859ba32d739`  
		Last Modified: Thu, 21 Aug 2025 19:12:03 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c549eca81d9d5e7c3800e8cd26f3b583548114f4bf15a7a2e68168083cc13a94`  
		Last Modified: Thu, 21 Aug 2025 19:12:05 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b715357487e09320e40d5e9b0e98ff762af0aff174994cee455b443b1095dd7b`  
		Last Modified: Thu, 21 Aug 2025 19:12:05 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6c17532ee009919ccbb8b2a5d5f664062b895578087722a29c00cf26cfb693ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5737511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1241e24268735dca8da5e754c482cbbb533ed699de1ab9e3b2fcf01140d415f3`

```dockerfile
```

-	Layers:
	-	`sha256:b6b99d3fd1a82cff246ed1bb07b492ec57686717bc5e2e6ec752d2ebdd1f242f`  
		Last Modified: Thu, 21 Aug 2025 20:11:36 GMT  
		Size: 5.7 MB (5694326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c09a4e552dc0a050e6f4a62a5585af2aa7192c9b262b66aa1692474328ab8f`  
		Last Modified: Thu, 21 Aug 2025 20:11:37 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e7f84c8f49603346131ef089394845c9ecbd88ba6c15bb6506330a1e26771fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446601239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cad73ae707126c10df2c623b46ba861554123f5b1fc829f8af0327c9ce6e59`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T16:35:56.587Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=616b79995b497dd1c83937d5f71450516b36b6fa org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T16:35:56.587Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=616b79995b497dd1c83937d5f71450516b36b6fa org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e8b56e4723ec079a70aa0cfe1546349f02500063f34e283876aa2ab251abb7`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 19.3 MB (19312287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdbcc1bdc8e9d63296b9af1e8a8dc7a21d50919098003d05990981079b03a7`  
		Last Modified: Thu, 21 Aug 2025 20:17:27 GMT  
		Size: 372.9 MB (372872133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecacdc1e82bae1336a5f868496082490036b10c0c58b1a2263364ced6049739`  
		Last Modified: Thu, 21 Aug 2025 19:29:45 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98d49777834e6231b46f62acf4667752989c5035a0b01da2248273771fd0ae7`  
		Last Modified: Thu, 21 Aug 2025 19:29:47 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e44e2a051903db75298c3f0a47b2a8460f6a4b6f74150cec01e81ec4f91ba2`  
		Last Modified: Thu, 21 Aug 2025 19:29:47 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24ff7adc0e05f6f22a4f8ef555f2ff812d1f7163cf6c464a47ec51d63c7e0a`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fdd72d2c2ec0f0c49ec37aeb770f4322eae34e5fd9ae7cad866deb034ab419`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b506bff6d6a3eba1015e548dfdfc541813a0a4b100470542d00122fce1153d`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4535616589f9fb339ba3b5017124a491c078205da02941e21e1b1872f3bd8156`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38002f388a488af3a9d147e8a19bb51da830157dde56638182d5d576a00804e8`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f986e94f02496027432df29df1e8d0786eb8877f799d5dcfa5230f8d8d1c1a`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec2a68583d9cd1b055a37984efc0b633ed3900bddebe84040d2844dc6e7b97`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.2` - unknown; unknown

```console
$ docker pull kibana@sha256:bde8e65f17af630cfd0b236c11b34c2eeba9d2f4fc2c9e968cac6ec3ab199981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5736446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2c73c44201842b1dbaf0ccf49670d080d68f1728d23e6153b78461b8c5b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:6a1a64c04325e4d8f9ec3884dd17dbc536452f5b78450f22e55c05319d2e18c0`  
		Last Modified: Thu, 21 Aug 2025 20:11:43 GMT  
		Size: 5.7 MB (5693004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98aa29fcf3d64a61f57b398e870373ce0a66e45480c071feb4196af3518568b3`  
		Last Modified: Thu, 21 Aug 2025 20:11:44 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
