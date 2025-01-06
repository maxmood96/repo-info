## `dart:beta-sdk`

```console
$ docker pull dart@sha256:6601ae030e7ea52d632aa42f61ec1957ef1d1ca64ccb2a6e1823d0f8ec5b3284
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
$ docker pull dart@sha256:d36fa76a07efe5f0960308823b4fa8091d86b68a053910e3c7f4159481d69d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302253276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e468d3410a17b0ea1887764121ee2e1b9e2deea205884ebe40ac7a1c830bbc21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Dec 2024 15:15:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3581dc339f4722cdcbf4acaccdc5209ab9f14d66502b396075c4d75df93a28c`  
		Last Modified: Tue, 24 Dec 2024 22:27:14 GMT  
		Size: 54.7 MB (54712058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bde3c34646b2288178d9182d706e6e54c5867c410b2a81c388de719dc145e7`  
		Size: 1.8 MB (1796908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a758db4e98c4d66f0d65b07fdb159e5bbb6ff8b24e3caa5666ec2975daf30c`  
		Last Modified: Tue, 24 Dec 2024 22:27:17 GMT  
		Size: 217.5 MB (217512697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:49a4705db1d5f4d794e4369c6a4c551e87be75a66e07befb3666794cf5419206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a55949c777cf73578ff7c5357b74b34f9f2d855c4a75997d2313d31139859`

```dockerfile
```

-	Layers:
	-	`sha256:61c5e74113fab83e0274d938a378ec7dccc1c20232d6fb40a304fc114e5bc7d5`  
		Last Modified: Tue, 24 Dec 2024 22:27:12 GMT  
		Size: 17.9 KB (17910 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cc73b3c2bbf28a2b0d21e1cfcc7784d9290011037adb307a283dd07739f20df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224753172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc62d8d2f24a5e2c2de1fb4c30ec53bdf459f3735c5172a621da6619983fe9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Dec 2024 15:15:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689318bf76a8dd4043ce70c82f26289471b16ae5819c010091389de80431b97b`  
		Last Modified: Wed, 25 Dec 2024 03:49:08 GMT  
		Size: 49.4 MB (49367345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c84d81f266ec2585355bd2e2ed55d6cd30d49f3236885c32df91cdf54f35ba`  
		Last Modified: Wed, 25 Dec 2024 03:49:06 GMT  
		Size: 1.2 MB (1221682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82857ad87744ffd556c2177c02088d914ca17c377ab029ccffe8b2f4fabb5d`  
		Last Modified: Wed, 25 Dec 2024 03:50:02 GMT  
		Size: 150.2 MB (150230591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:3c067a294b56b8ea4c26865542e0093694cead07223dc1647aca17be68842e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee943c04ec67dc5496128dd1ee252eaa33de1f3d1415ff1badc383f6e777e9bd`

```dockerfile
```

-	Layers:
	-	`sha256:d811f66e1e90d870183db5689368cab185f2a38b1dc53f9d6d40f73d7f328258`  
		Last Modified: Wed, 25 Dec 2024 03:49:58 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:43c316a828e82d7687baff2b57356e7985d4ea1de40f14ed648946ff124455d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300890930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ea07077874282ad993491ee173b59ff7b342afe7c47816774f4db797ea4e73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Dec 2024 15:15:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 11 Dec 2024 15:15:24 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 11 Dec 2024 15:15:24 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Dec 2024 15:15:24 GMT
WORKDIR /root
# Wed, 11 Dec 2024 15:15:24 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=3b8eee768198b0dec627afbfea7db0c0004d2c55d1ca999c7061590ebaade7cf;             SDK_ARCH="x64";;         armhf)             DART_SHA256=69a5c7a68599f109364cd26da77500d5b1e09a4dcba455c562b7b7e2a502e1e9;             SDK_ARCH="arm";;         arm64)             DART_SHA256=424e554d41159701cf7a2b537a07addc6ac641339f09e8b186ea07312d0dc212;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.7.0-209.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350b8ee3c923617f751426999c11c9ebb6d18fea5bdfbe043c10d7ab794508e0`  
		Size: 54.5 MB (54478718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644c7934a85b5386cf1664e7edcefe7194b3a4e888f05f1e989c0e505590ecfc`  
		Last Modified: Wed, 25 Dec 2024 01:56:23 GMT  
		Size: 1.5 MB (1488031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7cdb3f23a0e284f7eaf039dd5f863b7fad30f55ef69b9723556dec043a7db87`  
		Last Modified: Wed, 25 Dec 2024 01:57:19 GMT  
		Size: 216.9 MB (216865426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:63287855eac90a9f6686932558ad47bfc128824a7a22d48e3cf6df43387a11f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994be985f43c3e886fb7fbd2629092e0aabbc45e6f635b252d5723acfee61085`

```dockerfile
```

-	Layers:
	-	`sha256:db4d7fdfbf1141e953cf656d8243360bbbf2be849c059b38ddbd415752cde494`  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
