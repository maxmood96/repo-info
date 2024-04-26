<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.20`](#kibana71720)
-	[`kibana:8.13.0`](#kibana8130)

## `kibana:7.17.20`

```console
$ docker pull kibana@sha256:a37d81cb7c4f1735776ee5a1a15afaf3c1c1000a048bc43808da121ba880789b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.20` - linux; amd64

```console
$ docker pull kibana@sha256:add69da9f2e1464b3ddb56321794daa0b2eb81a37ad16d43b8a9b72dd0c3b021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366273453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3927dd7ea236bc9cae6b687159322299dd90a6737f569a5c8ad36afce70d8164`
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
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
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
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866b44bb9ab2f0d83a31557916e737ed8ced5a45163d36ebe64540eeef49a282`  
		Last Modified: Thu, 25 Apr 2024 21:52:53 GMT  
		Size: 17.3 MB (17289361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe48741b33b1ca416a8365c7485da7bbd2c90e01dffeebb99332a011414dc9c1`  
		Last Modified: Thu, 25 Apr 2024 21:52:53 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4e984952bf9de1a6c6ab05e8a1f93cb736f2bc0233c397bdbc5e67a97ab486`  
		Last Modified: Thu, 25 Apr 2024 21:52:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fe7dfcd8a0398d8b3a5ad367ab2fea71ed978ddc081a978b608bf2075949a6`  
		Last Modified: Thu, 25 Apr 2024 21:52:53 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab2b65ba394080111fc9c18e1b2258c47e6a4faf1b6df941706707161a2f0d`  
		Last Modified: Thu, 25 Apr 2024 21:52:53 GMT  
		Size: 5.3 KB (5301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c249496649d12e61e826c2cd94247ad918624da9ba470ff93edaca11c71566`  
		Last Modified: Thu, 25 Apr 2024 21:53:03 GMT  
		Size: 304.8 MB (304800150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53dddb0c01136af4466227b454badbd7cc20669522e2550d15e489098e8476f`  
		Last Modified: Thu, 25 Apr 2024 21:52:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c28a42f22a9344159e9380c578bb94d1b7f0f01655ff6496c6768925e4bf7c`  
		Last Modified: Thu, 25 Apr 2024 21:52:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe144ad7cc35f414b16a26945568352032c8cb8d1df09b67bdfe913c3f35a03d`  
		Last Modified: Thu, 25 Apr 2024 21:52:54 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4bbdcc988a8ecafc356986a570b5d0edb6fccdce05a6385c14ef0ea09ed765`  
		Last Modified: Thu, 25 Apr 2024 21:52:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c6d8181aa64298f92508fb13c5e630256c84d023116a557b367eb831aadb3`  
		Last Modified: Thu, 25 Apr 2024 21:52:55 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b77cf82fce622e9df9d1b9bcd638b347e28bab881462784639e7d31996f55e`  
		Last Modified: Thu, 25 Apr 2024 21:52:55 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:5811516caf20e5374e6ca3601471baa218219b8de71eaee0ddc02e03ed2478fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa575c0e7340cf5442ccf9a68fd1f2e695a0b6879264ee6b4f6ad20d1d572a5a`

```dockerfile
```

-	Layers:
	-	`sha256:08d9b771b88530ab758777c3e36c28c91cbcce809379900f9820c1a776346c26`  
		Last Modified: Thu, 25 Apr 2024 21:52:53 GMT  
		Size: 3.3 MB (3289966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336781d1971afe4774fb0d9e59ba6147d38de2a41ef4a51caf5f31b2049d2fa2`  
		Last Modified: Thu, 25 Apr 2024 21:52:53 GMT  
		Size: 44.4 KB (44367 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.20` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:4b71f9639d431a6e244968604d6ed2e208937eb7db36a676041a8763e119722d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.6 MB (375624733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2aa77ebb63af8ebd83b5a5d1355e1887a40cb32f8fdab75b75fe59df4604f7`
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
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
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
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62a3c46000da46c036cdd0d4b4f9f66e4dc83e26fcdc2d76cdd93e0d12036a8`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 16.1 MB (16074936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dbe09fcaacc3282a4c1c64c1a97b416525784c9b4abe505132e748e99868f5`  
		Last Modified: Fri, 26 Apr 2024 07:52:28 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfaf5a493c3ea17a51eb10a39e38e4c7492ddcad6e472042cbb25eb1b3c0c0a`  
		Last Modified: Fri, 26 Apr 2024 07:52:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d945f76b7ea70b5987540220a925852e2110e3ff25f4ef483f8c6102aabf46d`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10f67911506ae73c014286f9a09fd6097da56c2367dc90addea7b51caa9192`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a60d50bd947f08ea432b2962badacc5e7a408355ab9fe9cd82e1d3328fc24`  
		Last Modified: Fri, 26 Apr 2024 07:56:19 GMT  
		Size: 316.9 MB (316907906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf3b7f1f5533914e03334dadc9c2195d1d2c0b4e19cddfe37c90561c973a254`  
		Last Modified: Fri, 26 Apr 2024 07:56:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774785540418db3b3d82d97d4e9655d828e57c295ae1fd40f8b2906d13b70d7a`  
		Last Modified: Fri, 26 Apr 2024 07:56:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779e6df4eff27dddcf633669517314724c29cfc6251dcec4a70ce5a2ad9295e7`  
		Last Modified: Fri, 26 Apr 2024 07:56:12 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199556a4efe07fb446d82f63ccf958f30795d2d1c2dec77dcf3a0b1874f6d980`  
		Last Modified: Fri, 26 Apr 2024 07:56:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c958947cf28bc6ae8991ee1a365346e788a6b7227829633dff604daea4a07bb9`  
		Last Modified: Fri, 26 Apr 2024 07:52:31 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5846cba97b0e9fb9dfd6a590073456fd79fa90501ca3dbd63b9ce073583820a5`  
		Last Modified: Fri, 26 Apr 2024 07:56:13 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.20` - unknown; unknown

```console
$ docker pull kibana@sha256:c35133dcee163c9daea56e13d771194b3812e30b6d96421598bc751a1e9f6df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3334411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1496234b4a3c0336e544b615328db83513554343e58874d2511792ad8d6edd4f`

```dockerfile
```

-	Layers:
	-	`sha256:f979f775b29825d3879282cf840f74854cdc92eefbbddde142d7f01c2e430681`  
		Last Modified: Fri, 26 Apr 2024 07:56:12 GMT  
		Size: 3.3 MB (3290201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04d8c53d79dfe5d7e8a8e3052992ce508ff7a35b63c1d691d2c873834d229dd5`  
		Last Modified: Fri, 26 Apr 2024 07:56:12 GMT  
		Size: 44.2 KB (44210 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.13.0`

```console
$ docker pull kibana@sha256:3dea42a4a752b973fc7534b3c8ba7bec1e94f5c8593714e547b77e83f7e954f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.13.0` - linux; amd64

```console
$ docker pull kibana@sha256:4903ac75be20f9dd4980d9ad6200f07430ebbd5762a2a83fa75d6fe7b99dcb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.6 MB (381637337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af33ed45c338045ccead8b466c3be2a2695cddccecefc9e0e73e506b126d31ca`
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
ADD file:f0e219aa0262921f4667bb1a79ad839b3efd92e23eef2d1b5eba9cfe4eaf78cc in / 
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
	-	`sha256:4477f8fe99ebfd23fa06d28a2fa42eaa05d726926afc0a055e1ff2b612b7a293`  
		Last Modified: Wed, 17 Apr 2024 18:54:17 GMT  
		Size: 27.5 MB (27511740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46ab79bd0d53b4243fe75eeefe471ef49e8ff5860e5a9e3d8fce4b88facd554`  
		Last Modified: Thu, 25 Apr 2024 21:53:51 GMT  
		Size: 17.3 MB (17289328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdb8732325d0fc3f65297dffeedea0153c6d0a2b9887621d3a1a2561722b375`  
		Last Modified: Thu, 25 Apr 2024 21:53:51 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f40af64eb2de77ec6f44d0f0091df9ae00b3fc7b649b90e158a65bd8f0fa9e`  
		Last Modified: Thu, 25 Apr 2024 21:53:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85977aeb81e64105739b4ca936303dc7b6453ce57eeb20ff349d094a25d48709`  
		Last Modified: Thu, 25 Apr 2024 21:53:51 GMT  
		Size: 16.5 MB (16460479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43e22bcd2740c09a9a6ab834ecd997b7d40e9c4e5a32b70b6d530c5d129b3e`  
		Last Modified: Thu, 25 Apr 2024 21:53:52 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1924d7b6e495f1aba3c9ae088c3b9a046da5cc1f517dba74dc038873358fdef8`  
		Last Modified: Thu, 25 Apr 2024 21:53:56 GMT  
		Size: 320.2 MB (320164036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b54dcac1ec3d47cc345f23b4d8280d7b662c0723c3752cb0ccdcbab5e591b2a`  
		Last Modified: Thu, 25 Apr 2024 21:53:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0716a252f1d8ac1f46ad3d673e1d60494a26672ae913bb1b29c0dc847a54e8b`  
		Last Modified: Thu, 25 Apr 2024 21:53:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aec58de297b16842d5658f381fc2d6d5b816f51108f09375743cb091052397`  
		Last Modified: Thu, 25 Apr 2024 21:53:53 GMT  
		Size: 4.6 KB (4565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db58bb281992b10b7c63daee205ad913630565ec2776127e0c5d5272e2a2c778`  
		Last Modified: Thu, 25 Apr 2024 21:53:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de09e033fe9722f5744306da7edf7db52266f3819d15638fa99158c6e0a40c73`  
		Last Modified: Thu, 25 Apr 2024 21:53:53 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294516f8343e1b05769b619f524545d1bf284fc78b9b2ccd2f7570fe1f7caaef`  
		Last Modified: Thu, 25 Apr 2024 21:53:54 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:637ce8d35b203f530fc132f40690ba4510c3548ba4b5179cfa72f29ef8135b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa41121fa099a1c50b04e794ac8904d49bdad20650c290276f6abf65da685c3`

```dockerfile
```

-	Layers:
	-	`sha256:444723f3979ab9ddcbdbb2b02ffa62bf60617dc75697fc43a156d68564bb75c9`  
		Last Modified: Thu, 25 Apr 2024 21:53:51 GMT  
		Size: 3.7 MB (3749657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145e7a631636a769306d2742b415dc0e80709b4e637f5ecb997b739b5b6517c4`  
		Last Modified: Thu, 25 Apr 2024 21:53:51 GMT  
		Size: 44.4 KB (44356 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.13.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:8f72064b715161853b4194876861569d06691da6fc916c8fe6705fa5261cb98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 MB (391011269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcd3a61ee600b896c249b435dd477f1863210a665244e7336307c6b056108fa`
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
ADD file:14fd903d8c1e98bd6a8c31b38182fa528e5277243e3b7ea9f682a57a9e7a3e60 in / 
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
	-	`sha256:935803725f5775642918295f3557fecf93003fde6403df6fcbb2379ce4795a1d`  
		Last Modified: Wed, 17 Apr 2024 18:54:25 GMT  
		Size: 26.0 MB (25976141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62a3c46000da46c036cdd0d4b4f9f66e4dc83e26fcdc2d76cdd93e0d12036a8`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 16.1 MB (16074936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dbe09fcaacc3282a4c1c64c1a97b416525784c9b4abe505132e748e99868f5`  
		Last Modified: Fri, 26 Apr 2024 07:52:28 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfaf5a493c3ea17a51eb10a39e38e4c7492ddcad6e472042cbb25eb1b3c0c0a`  
		Last Modified: Fri, 26 Apr 2024 07:52:28 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d945f76b7ea70b5987540220a925852e2110e3ff25f4ef483f8c6102aabf46d`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10f67911506ae73c014286f9a09fd6097da56c2367dc90addea7b51caa9192`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 5.3 KB (5288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9287a4bdf3587ff23c5b6b7ee72e8307b3a08e225ddf74288ec44c6e93738f29`  
		Last Modified: Fri, 26 Apr 2024 07:52:38 GMT  
		Size: 332.3 MB (332294386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a03c6cc21af7cf303d373c1c3fd52617539c7be65ee2097b4f90dfcb5869db2`  
		Last Modified: Fri, 26 Apr 2024 07:52:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd06ae5f52aa4ada4709e3a50a470d904f3cbcbfd4a429fa8b40e5a20d98c16`  
		Last Modified: Fri, 26 Apr 2024 07:52:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba52b7b0a9daa802e47b2c3aa853696855da9bd24beb227307d5f2935ebadfd`  
		Last Modified: Fri, 26 Apr 2024 07:52:31 GMT  
		Size: 4.6 KB (4562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af31df812967824a39f0da2c40d4fb2a09ca5369da7e46cfa996321a2e77a7a`  
		Last Modified: Fri, 26 Apr 2024 07:52:31 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c958947cf28bc6ae8991ee1a365346e788a6b7227829633dff604daea4a07bb9`  
		Last Modified: Fri, 26 Apr 2024 07:52:31 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa5c3535a432a840ce165ebf273798afc0c97bf99726d8dbeb93df8228e2acd`  
		Last Modified: Fri, 26 Apr 2024 07:52:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.13.0` - unknown; unknown

```console
$ docker pull kibana@sha256:a4c7dc992c78d1bd88cfe4fa3e735171acb726303693396a14239219366cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631fb6c4921234aea7d5be202bbcd635102a3a8fae14089e06a01e5fb46901df`

```dockerfile
```

-	Layers:
	-	`sha256:d76795d1fd5bd75bef2f2204698730bfd8ababe8c850d7f3f78f8fbe01f1a83e`  
		Last Modified: Fri, 26 Apr 2024 07:52:29 GMT  
		Size: 3.7 MB (3749892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acecfddc4383da613dd82298cae6ac733d85a233f10907cbb4cbece69393a465`  
		Last Modified: Fri, 26 Apr 2024 07:52:28 GMT  
		Size: 44.2 KB (44199 bytes)  
		MIME: application/vnd.in-toto+json
