## `dart:beta-sdk`

```console
$ docker pull dart@sha256:904e90c838fe0f70c478adcb8abb520380bf9be9f747ece30af6f7f5fb57c340
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:659c1501cf02b0f21a4ffd53b8997fe25d2d4a956e64e7c07988bcccef9d08ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304792577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5878d61e671d976f90eb43c4e9a93b5d072c7f4810d3323cbcaef61aeaf0ccd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 30 Jan 2025 08:39:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Thu, 30 Jan 2025 08:39:20 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 30 Jan 2025 08:39:20 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 08:39:20 GMT
WORKDIR /root
# Thu, 30 Jan 2025 08:39:20 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=77a239e591f2191ce0f1a7303ef536de4103ed4dd45201b08c77a67ee9cb09f5;             SDK_ARCH="x64";;         armhf)             DART_SHA256=2ccdf0b9c0b7cd59c4993fdda32ec36e90c56deacc43bd58087ced4b23f198d5;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6b865b4447eeb71b5f6b179e1c38bba0f758b808baae48eac80f9348801b67e;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-323.2.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5385fb88aa23fb935cf7e52dca4b4f05b1bdd1eccf5aa0cf4a18be210105f2`  
		Last Modified: Tue, 04 Feb 2025 19:32:58 GMT  
		Size: 54.9 MB (54906681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30514d202daad92a9467c3613526b164fa603c35330feda04b1d625137994ad9`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 1.8 MB (1796916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1b654771c20f95f5342cbd0387d3c08d9b342d274ceeffd676bb93607d0e94`  
		Last Modified: Tue, 04 Feb 2025 19:33:00 GMT  
		Size: 219.9 MB (219876645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:435f8a7d58943d058226f46d70ca967d02cfe74136a7ee6bde6aceadeb53fa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dcccbf7cf1f27a33a31431ccd5258649bd69b58f8c869331ef3189c3afa790`

```dockerfile
```

-	Layers:
	-	`sha256:84c8a26fccabb9e8e022a29c10134da751cb90b2ae3a6f5551f0fc0eb54626b4`  
		Last Modified: Tue, 04 Feb 2025 19:32:57 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:d4e0395e52c2cae1cf1fd799039b7dcaf3dad424220c2e1fdbeb5d3d791ec0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224928443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264477b92316c8ff78809907e27077229e47eec70e21874b5da54d5ce748f33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 01:37:24 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8af8a5133a30e975a3b9d74bf15cc52f8d673450261b1a58fdfcd7f3a20aeb`  
		Last Modified: Tue, 04 Feb 2025 10:50:18 GMT  
		Size: 49.6 MB (49561568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17612930c2cc3b54370d8e7a9709ce77958469f4b54a2958676f7545909b77e`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 1.2 MB (1221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21316a5b5b0d4084df0abf17c5b0bf5d6672435763f3c2fd27a4aeb8147a6be5`  
		Last Modified: Tue, 04 Feb 2025 10:50:21 GMT  
		Size: 150.2 MB (150230626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:939e154100cff3d2ab12b41cdb8d198adc770a8ed76478585802d223e124841e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17a53a5437bcc22bb8fe18a0bee266234cec83fdad76f071a6c8150ce5e0c6`

```dockerfile
```

-	Layers:
	-	`sha256:bc72fa39423d4a92a051ffbb23a6e51a7775cf8565521c793d0656b202e8c587`  
		Last Modified: Tue, 04 Feb 2025 10:50:17 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4fe4a41963df49f4c24e5ee381239c4a1497acd3a1bd2ba59d32f817454e22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301072649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd01113aef7e9ee6ae16d7087f3d9a349b98d1485458460a4fd258029cbc98`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 14:24:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 08 Jan 2025 14:24:09 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 08 Jan 2025 14:24:09 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Jan 2025 14:24:09 GMT
WORKDIR /root
# Wed, 08 Jan 2025 14:24:09 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126af0939b0f0fe80d45e16234ab959ce4b7569c531cbe68fecd59ad47ae146`  
		Last Modified: Tue, 04 Feb 2025 09:15:07 GMT  
		Size: 54.7 MB (54678176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76895c45ded445277d80dfcaee0f604a00263996e451eac21374f668be3a475`  
		Last Modified: Tue, 04 Feb 2025 09:15:05 GMT  
		Size: 1.5 MB (1488029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd8ed7ce48c978d4b970a58ac366fd020a171b48eb7b7c8b925cb603573ea4`  
		Last Modified: Tue, 04 Feb 2025 09:16:05 GMT  
		Size: 216.9 MB (216865531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8de859316e0a14bb4af8488e3cf495f6627c554bbbab5067d2035a964224f7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadb2251094063505f367d15f604396559a03902f2d51d50f9ec86f9639ed71a`

```dockerfile
```

-	Layers:
	-	`sha256:30ea7807006b7d88217ae6800be9977d5384d0c84b8013037bebf62974c4ef2a`  
		Last Modified: Tue, 04 Feb 2025 09:15:59 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
