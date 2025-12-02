<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.9.4`](#api-firewall094)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.9.4`

**does not exist** (yet?)

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:450e70f1bb728c960e92242ef0525588126fe804303aed63ea19b33449b9acf8
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
$ docker pull api-firewall@sha256:744fb532234b0a611ac6a72480355a950d3cf0cea352949ddf2aca7f80a4f434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17155795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d487ac27c315b61e6e7227514cec1c3f94bcc4b98827639cef09498699d1d9bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 19 Aug 2025 09:20:01 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2011ad4bdbaeb9ee48cdb7dd1ff71a725a1d94057e4ea7fb4bf496fedc96c26`  
		Last Modified: Wed, 08 Oct 2025 22:17:05 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c575d59514ea23ff4555ebb900eaa980620ab5f82f8a9d4286d67eca962fa97`  
		Last Modified: Wed, 08 Oct 2025 22:17:05 GMT  
		Size: 13.4 MB (13352091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf7480684e6137a12fa5c04e10ea7a3601353a0dff1e381984949bc266c650`  
		Last Modified: Wed, 08 Oct 2025 22:17:04 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:0983755d5a6df5ab9912a314f8d76c2cd2718788ff3f9b5668bc3970cb7cccb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a93c286a6274ed96fbf90687076c99efb8171decc39978e368df9dff54454b`

```dockerfile
```

-	Layers:
	-	`sha256:8bd23d79d09a2eb955a213fb16ba319b34cce4ccae617895fbd79e324187fca2`  
		Last Modified: Wed, 08 Oct 2025 23:44:24 GMT  
		Size: 164.6 KB (164574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564f2a2ea052f808eea1c65d2c6fe0ab18423c0a5f966059aa9e18941f82dbd6`  
		Last Modified: Wed, 08 Oct 2025 23:44:24 GMT  
		Size: 13.5 KB (13546 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:9d79c50189be9647a3b8fdf0df87da1d2cf554eff4cb747ef76330adc2713ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16430944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5885ea41f6eff70cc7864d04779ad0e5502e9adf7a12512e6429d903c9edd438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 19 Aug 2025 09:20:01 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea23a53fae849354d6455ef7f5963cd0a6f1f43e73448aece561e39c57798bce`  
		Last Modified: Wed, 08 Oct 2025 21:13:08 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08881b5f87537154409a8e6d14c3ea2379a1607f53446e579f4cbee936a06642`  
		Last Modified: Wed, 08 Oct 2025 21:13:09 GMT  
		Size: 12.3 MB (12291622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51384b13617667cb66fc4ee60448c844ce0a26bea3b99923dd36ce54b6fe3e2`  
		Last Modified: Wed, 08 Oct 2025 21:13:08 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:7cec555327f5f7275d7f61bff1087c54a57d2ef7e0185e251209e39e1751e334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 KB (178247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e1c20e32da9c820d680f16d95ba78e2b25c5c82696b78d3331bc59f57e9370`

```dockerfile
```

-	Layers:
	-	`sha256:4d3f285d59b265aea0719bb1dfe91531dc99de164ed0e6964235a229bbf1a4cd`  
		Last Modified: Wed, 08 Oct 2025 23:44:28 GMT  
		Size: 164.6 KB (164606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75cf3770641afdbc6dcba20610203b8fa99ea00b8417712c0bbbcbea6d1816`  
		Last Modified: Wed, 08 Oct 2025 23:44:29 GMT  
		Size: 13.6 KB (13641 bytes)  
		MIME: application/vnd.in-toto+json

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:fc60bc6605c642cb7ec1676f3bd3b212d8b3f0fdd9ebca73a07a0b29f1d5f8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15441208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1dae3f148ae154b6f1342102a655bf081c13e1e7a08673255e192b70ecca528`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Tue, 19 Aug 2025 09:20:01 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFW_PATH=/opt/api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
ENV APIFIREWALL_VERSION=v0.9.3
# Tue, 19 Aug 2025 09:20:01 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='85c3345fd60bb2ad4910674fd0d7311dc002e8ad475bbc1f8248463b94cf3be9';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='61ae4b3c0576eada59e306c2f757bb737853198228b64577abf9c7781f0a6fbc';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='4bb62a6332f29d86f8da77a3cc95be61c3db596f0c4b1cf6b3ed81c83f6cf8df';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
COPY docker-entrypoint.sh /opt/api-firewall/ # buildkit
# Tue, 19 Aug 2025 09:20:01 GMT
USER api-firewall
# Tue, 19 Aug 2025 09:20:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 09:20:01 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52352d30c02147a7b9060ad5b4fceb817793b23a3ec6e2ebc5015545dbb2f75d`  
		Last Modified: Wed, 08 Oct 2025 21:20:22 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3cfda496a88cd93e1b270473fe073875f32ed7dcfeb946132dfc0620e18a13`  
		Last Modified: Wed, 08 Oct 2025 21:20:23 GMT  
		Size: 11.8 MB (11821023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e26ff660685338e5c140f472969e22c89d4d97a607316ecd7b402ed6142a81`  
		Last Modified: Wed, 08 Oct 2025 21:20:22 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `api-firewall:latest` - unknown; unknown

```console
$ docker pull api-firewall@sha256:516a748cf5fcb901f483f31c914a8b23c691e555f5383c47911e81e9051ef814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 KB (178081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90553dbddef24cbd7b9ad726737bd498dc87ef1120ba901cf6434cdaaaa5761b`

```dockerfile
```

-	Layers:
	-	`sha256:d2f18fa305cabc98093d3acd2faaf016121ea7a38f6f601c74621662a4157e6c`  
		Last Modified: Wed, 08 Oct 2025 23:44:32 GMT  
		Size: 164.6 KB (164559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ac2540f1ebd26483f387e1c01c1ca057c27774b1efa6c776eb5e596c54bb19`  
		Last Modified: Wed, 08 Oct 2025 23:44:32 GMT  
		Size: 13.5 KB (13522 bytes)  
		MIME: application/vnd.in-toto+json
