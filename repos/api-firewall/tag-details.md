<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.1`](#api-firewall091)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.1`

```console
$ docker pull api-firewall@sha256:221c12cc1091184e086688913763df57a28166c675a521cc6feff7b10c52ab17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:0.9.1` - linux; amd64

```console
$ docker pull api-firewall@sha256:971c7993b65970ea425b3f0d37f5d884d2dcb9c379b380445cf10f5fac024a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16374046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4904547c6f0c132798541368d2882d208e6db59854cc4d9a2c4100bc14649e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 23 Apr 2025 16:58:29 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb1a6a86df3bdc01c9893d6efee89b7052eed78c22923bf6c929dabee2c9c91`  
		Last Modified: Tue, 15 Jul 2025 19:11:25 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac64ea169a4dc0c9c51b0405774837bbe1fd3e948cb9b381c0402ef58730cc6d`  
		Last Modified: Tue, 15 Jul 2025 19:11:28 GMT  
		Size: 12.7 MB (12735227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4c98bd5d3c1ecae11e0b6443e5b58941303141f8c34d2529a70d9d548d6c36`  
		Last Modified: Tue, 15 Jul 2025 19:11:26 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.1` - unknown; unknown

```console
$ docker pull api-firewall@sha256:6d522660c861e17777f0bcf7a030b3253d1cedb56142b2c9e938f79af732932d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 KB (172450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9399fb6fb65229606a3ef720136cad6ce86ccc4acc05dd093bd33a231d54ea8`

```dockerfile
```

-	Layers:
	-	`sha256:2340139777f291a8b13509686661b16467385ee35f67ddb21ba979625e04c75f`  
		Last Modified: Tue, 15 Jul 2025 20:44:24 GMT  
		Size: 158.9 KB (158905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cac4e85c6c1e98f4f2589b4a782b51192b651e4df6714aba24a431edd7a90ed6`  
		Last Modified: Tue, 15 Jul 2025 20:44:25 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.1` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:8ecdad599a1012f69bda42aefe1a360736bd9433d8eacafc0036092120766c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15728349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a8a14cd097896986cf8a1856d658e11d0b3b0c6cd8e64f169ca2ad27b6e19d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 23 Apr 2025 16:58:29 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90613bcf6d1e62b5df393fed684a5da2bd092cd930b83ac3f770cca1fd7b24`  
		Last Modified: Tue, 15 Jul 2025 19:11:51 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf25af80a2bd3ec45568b84a105b44a87b09efb7706764cad5f7411d9ae3cba`  
		Last Modified: Tue, 15 Jul 2025 19:11:54 GMT  
		Size: 11.7 MB (11740163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7160532bdaf87ae278fcc87267dcfb75a74acce75e9b04481287f4bc792bd15f`  
		Last Modified: Tue, 15 Jul 2025 19:11:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.1` - unknown; unknown

```console
$ docker pull api-firewall@sha256:eab048877b06b0d020c0071e26939d60d80e87218413423a6fd20cac1ee5f268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 KB (172578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0713f2c67ded4be69d2e4537592704b4eed7197ac2428ec040af5d37d50dc23a`

```dockerfile
```

-	Layers:
	-	`sha256:f0e22caa6cdc6012a12875a6282ff01fa0f56c59f33d78e0ad37fe0da3ffe231`  
		Last Modified: Tue, 15 Jul 2025 20:44:28 GMT  
		Size: 158.9 KB (158937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed31d251e3adc52d3837a338ef1410fde0b6d00ce5699243a5bde6291dd590`  
		Last Modified: Tue, 15 Jul 2025 20:44:29 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:0.9.1` - linux; 386

```console
$ docker pull api-firewall@sha256:25a1a404123093f9410f9bfe77a932bbb51c6b486d58e33d7cbb048e88403a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14628442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfdf3c605f69bca5798343280b42c2a9f2d51c21f84eaf8c96a968afb683c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 23 Apr 2025 16:58:29 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242fc15be7aac2403512a4fc34b674e765f3f5f0f27807a119ca7ab1407c5fec`  
		Last Modified: Tue, 15 Jul 2025 19:11:05 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a51ff45f54cf395327b569017970963cbd7ec5a9f5178db3631c866c02202`  
		Last Modified: Tue, 15 Jul 2025 19:11:05 GMT  
		Size: 11.2 MB (11166469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e617dc0c2a0e476e636d9ee56b8d52ec15d32ee77440fed35ea480c6cb3b29`  
		Last Modified: Tue, 15 Jul 2025 19:11:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:0.9.1` - unknown; unknown

```console
$ docker pull api-firewall@sha256:d3c7a655536e719993086817b43e0230d711532323736daaf0a2829c2f5096be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 KB (172412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e322205eda5bb0dfe7f421b908e72f0aa634109c0ab320d92a88ba6edc4ab58a`

```dockerfile
```

-	Layers:
	-	`sha256:b8f1bac17d9f8b3315764f77a9fbd077f6be875c7ef55203900fac011fb633b3`  
		Last Modified: Tue, 15 Jul 2025 20:44:32 GMT  
		Size: 158.9 KB (158890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b432c026ceef2858acc5b06cfad9cb4ed8e653d350fb3df4333b6bb8e52c73`  
		Last Modified: Tue, 15 Jul 2025 20:44:33 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:221c12cc1091184e086688913763df57a28166c675a521cc6feff7b10c52ab17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:971c7993b65970ea425b3f0d37f5d884d2dcb9c379b380445cf10f5fac024a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16374046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4904547c6f0c132798541368d2882d208e6db59854cc4d9a2c4100bc14649e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 23 Apr 2025 16:58:29 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb1a6a86df3bdc01c9893d6efee89b7052eed78c22923bf6c929dabee2c9c91`  
		Last Modified: Tue, 15 Jul 2025 19:11:25 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac64ea169a4dc0c9c51b0405774837bbe1fd3e948cb9b381c0402ef58730cc6d`  
		Last Modified: Tue, 15 Jul 2025 19:11:28 GMT  
		Size: 12.7 MB (12735227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4c98bd5d3c1ecae11e0b6443e5b58941303141f8c34d2529a70d9d548d6c36`  
		Last Modified: Tue, 15 Jul 2025 19:11:26 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:6d522660c861e17777f0bcf7a030b3253d1cedb56142b2c9e938f79af732932d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 KB (172450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9399fb6fb65229606a3ef720136cad6ce86ccc4acc05dd093bd33a231d54ea8`

```dockerfile
```

-	Layers:
	-	`sha256:2340139777f291a8b13509686661b16467385ee35f67ddb21ba979625e04c75f`  
		Last Modified: Tue, 15 Jul 2025 20:44:24 GMT  
		Size: 158.9 KB (158905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cac4e85c6c1e98f4f2589b4a782b51192b651e4df6714aba24a431edd7a90ed6`  
		Last Modified: Tue, 15 Jul 2025 20:44:25 GMT  
		Size: 13.5 KB (13545 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:8ecdad599a1012f69bda42aefe1a360736bd9433d8eacafc0036092120766c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15728349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a8a14cd097896986cf8a1856d658e11d0b3b0c6cd8e64f169ca2ad27b6e19d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 23 Apr 2025 16:58:29 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90613bcf6d1e62b5df393fed684a5da2bd092cd930b83ac3f770cca1fd7b24`  
		Last Modified: Tue, 15 Jul 2025 19:11:51 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf25af80a2bd3ec45568b84a105b44a87b09efb7706764cad5f7411d9ae3cba`  
		Last Modified: Tue, 15 Jul 2025 19:11:54 GMT  
		Size: 11.7 MB (11740163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7160532bdaf87ae278fcc87267dcfb75a74acce75e9b04481287f4bc792bd15f`  
		Last Modified: Tue, 15 Jul 2025 19:11:53 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:eab048877b06b0d020c0071e26939d60d80e87218413423a6fd20cac1ee5f268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 KB (172578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0713f2c67ded4be69d2e4537592704b4eed7197ac2428ec040af5d37d50dc23a`

```dockerfile
```

-	Layers:
	-	`sha256:f0e22caa6cdc6012a12875a6282ff01fa0f56c59f33d78e0ad37fe0da3ffe231`  
		Last Modified: Tue, 15 Jul 2025 20:44:28 GMT  
		Size: 158.9 KB (158937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed31d251e3adc52d3837a338ef1410fde0b6d00ce5699243a5bde6291dd590`  
		Last Modified: Tue, 15 Jul 2025 20:44:29 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:25a1a404123093f9410f9bfe77a932bbb51c6b486d58e33d7cbb048e88403a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14628442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcfdf3c605f69bca5798343280b42c2a9f2d51c21f84eaf8c96a968afb683c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 23 Apr 2025 16:58:29 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
ENV APIFIREWALL_VERSION=v0.9.1
# Wed, 23 Apr 2025 16:58:29 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='f4f3a1e79386fd4416e8008a7a597e2e054011567dd688dabfe22f1735619d07';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c10aa8975086c77c32186528cc199e5968621da82994097e58a2c33f50082072';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8aea4ccc9085e75ae4952897a780c84618f8407ff6df34126be45560eed3a8c2';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Wed, 23 Apr 2025 16:58:29 GMT
USER api-firewall
# Wed, 23 Apr 2025 16:58:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 16:58:29 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242fc15be7aac2403512a4fc34b674e765f3f5f0f27807a119ca7ab1407c5fec`  
		Last Modified: Tue, 15 Jul 2025 19:11:05 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a51ff45f54cf395327b569017970963cbd7ec5a9f5178db3631c866c02202`  
		Last Modified: Tue, 15 Jul 2025 19:11:05 GMT  
		Size: 11.2 MB (11166469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e617dc0c2a0e476e636d9ee56b8d52ec15d32ee77440fed35ea480c6cb3b29`  
		Last Modified: Tue, 15 Jul 2025 19:11:05 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:d3c7a655536e719993086817b43e0230d711532323736daaf0a2829c2f5096be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 KB (172412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e322205eda5bb0dfe7f421b908e72f0aa634109c0ab320d92a88ba6edc4ab58a`

```dockerfile
```

-	Layers:
	-	`sha256:b8f1bac17d9f8b3315764f77a9fbd077f6be875c7ef55203900fac011fb633b3`  
		Last Modified: Tue, 15 Jul 2025 20:44:32 GMT  
		Size: 158.9 KB (158890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b432c026ceef2858acc5b06cfad9cb4ed8e653d350fb3df4333b6bb8e52c73`  
		Last Modified: Tue, 15 Jul 2025 20:44:33 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json
