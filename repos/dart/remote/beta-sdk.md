## `dart:beta-sdk`

```console
$ docker pull dart@sha256:ce9cb777f8ded07dfa20dcd6cbdc74c02d6d69c7c41ed3f97cb8a4339654a552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:32110bcd8a11eef24f4bd3953e5237e33fac1842854b48808fd30e4f109c52ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313909383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160f5a458dc414836a7087f840a3fc4b8693e5c26aade02a297505e413965da6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 17:45:30 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 17:45:31 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 15 Apr 2026 17:45:31 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 15 Apr 2026 17:45:31 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 17:45:31 GMT
WORKDIR /root
# Wed, 15 Apr 2026 17:46:36 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=64567d16674aa558a059d3c1af2dcde5fe222e166d092b11a721285d41361679;             SDK_ARCH="x64";;         armhf)             DART_SHA256=df9611c016da694f1d36dd923fc392bb1d5f9b3b5b8bf93d2367afdeb8522908;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e211c35ce943eea9f2038c0ef351bad325ba959d7c58cf4e77f6eacc02389459;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=a0b2e7509e369ffb8f531526f7fb60003fda4bbee0da938fafa282d5c6e78c53;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674b980416618b1d257b8874b797efb3b26d0d11e0b8a24b7b9bb76c58197ba4`  
		Last Modified: Wed, 15 Apr 2026 17:46:14 GMT  
		Size: 45.5 MB (45466346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f0921c286a628bd65d0e9dafeac953916d3d68e67fda1af4a3938283d97b4`  
		Last Modified: Wed, 15 Apr 2026 17:46:13 GMT  
		Size: 1.9 MB (1869571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12f991d28e4939688a08400d29ae2e35de70b1b7a75948e2fa5f6834a69bb4b`  
		Last Modified: Wed, 15 Apr 2026 17:47:12 GMT  
		Size: 236.8 MB (236797794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:ce02d659b1ce939346d1da15b317b8082efc07b70045f3e5b5ca5704aa96aa44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5257a9e60fee953aee100144a5e6d02cbaca9bfcfcdf8856278267aa1eade8`

```dockerfile
```

-	Layers:
	-	`sha256:454f2c9b5979537fdd2f03ab467992be01293b26de3150099d936e8d4a1c42ff`  
		Last Modified: Wed, 15 Apr 2026 17:47:06 GMT  
		Size: 18.9 KB (18923 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:cf09a79a6b64898689d82d348d20c8c43e0a0b817198ef703bad725a757542c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228276843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3a552cdae2d6c753d26627d07565af3be5b46b40850ac7004754c4481141c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 17:45:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 17:45:41 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 15 Apr 2026 17:45:41 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 15 Apr 2026 17:45:41 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 17:45:41 GMT
WORKDIR /root
# Wed, 15 Apr 2026 17:46:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=64567d16674aa558a059d3c1af2dcde5fe222e166d092b11a721285d41361679;             SDK_ARCH="x64";;         armhf)             DART_SHA256=df9611c016da694f1d36dd923fc392bb1d5f9b3b5b8bf93d2367afdeb8522908;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e211c35ce943eea9f2038c0ef351bad325ba959d7c58cf4e77f6eacc02389459;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=a0b2e7509e369ffb8f531526f7fb60003fda4bbee0da938fafa282d5c6e78c53;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af39301a6057b453a1a2313cf921346b9530df78fd110b43eec08b0379c576d`  
		Last Modified: Wed, 15 Apr 2026 17:46:11 GMT  
		Size: 39.7 MB (39712819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbccf60244dc7e9c779fffd1f0bc51c869fc664c4b6e8d6ea2902600b2587570`  
		Last Modified: Wed, 15 Apr 2026 17:46:09 GMT  
		Size: 1.3 MB (1273163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602c63e16073363c6bb8edbf5bc927bc3b9403988f3e7604fec9ce0e7c64614f`  
		Last Modified: Wed, 15 Apr 2026 17:46:53 GMT  
		Size: 161.1 MB (161081176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:2ab64917565011d5b69cb15334cea3858a4d03cf52117ee72175a806166ab031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (19028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15aaeb922fad747889f20d63c9af0848e263e2039521572bbf975a98d42fe9d`

```dockerfile
```

-	Layers:
	-	`sha256:baebe9306e8c8803edd990b7670ac76f8c27c601f210ab0ca38b2f5d0799ebae`  
		Last Modified: Wed, 15 Apr 2026 17:46:48 GMT  
		Size: 19.0 KB (19028 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:4564dd5f3b653664a569ea9d506897b871760b5f2a6112fe847e7e3d2a261741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312722496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be074c5f27cb3a65c31fea7ddec833b15b1b321bc428920d7b74fb09d6194815`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 17:45:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 17:45:29 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 15 Apr 2026 17:45:29 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 15 Apr 2026 17:45:29 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 17:45:29 GMT
WORKDIR /root
# Wed, 15 Apr 2026 17:46:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=64567d16674aa558a059d3c1af2dcde5fe222e166d092b11a721285d41361679;             SDK_ARCH="x64";;         armhf)             DART_SHA256=df9611c016da694f1d36dd923fc392bb1d5f9b3b5b8bf93d2367afdeb8522908;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e211c35ce943eea9f2038c0ef351bad325ba959d7c58cf4e77f6eacc02389459;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=a0b2e7509e369ffb8f531526f7fb60003fda4bbee0da938fafa282d5c6e78c53;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d631e90406d2a749d241f4ea14daf120c4c93e8a06cb7acc11375668337a99`  
		Last Modified: Wed, 15 Apr 2026 17:46:14 GMT  
		Size: 45.6 MB (45617029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061a76c58dc72c9a03581a77c0dd9663674f3d916b592bc8e8c87e2d3d23ef40`  
		Last Modified: Wed, 15 Apr 2026 17:46:12 GMT  
		Size: 1.6 MB (1564341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b27660861319900b23eb8f839aed3f2478405b1389ffa0287bea6eada2b0ed9`  
		Last Modified: Wed, 15 Apr 2026 17:47:16 GMT  
		Size: 235.4 MB (235402543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:10ad71ca0cc56f4193cc2e1c69529f39ef0165cef731293576c5687e0b44fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274e0d592916eadce6a9a92e33b6171e5cb2deb0eaf6fae9a4e9692a70583418`

```dockerfile
```

-	Layers:
	-	`sha256:01c9655f9d55df3dce773a35b898fd371c2d723c299dfb9915e817216501606c`  
		Last Modified: Wed, 15 Apr 2026 17:47:08 GMT  
		Size: 19.1 KB (19057 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta-sdk` - linux; riscv64

```console
$ docker pull dart@sha256:bd4db99b405505a9d0a4abc7913602368c005a5ecf8458e8a4a5624123e22552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250940694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86537e85f22ee58b5e16bef83f8018a8c287fdba29dd27178ef37a531fdf5525`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 17:55:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 17:55:21 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         riscv64)             TRIPLET="riscv64-linux-gnu" ;             FILES="/lib/ld-linux-riscv64-lp64d.so.1                 /lib/riscv64-linux-gnu/ld-linux-riscv64-lp64d.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Wed, 15 Apr 2026 17:55:21 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 15 Apr 2026 17:55:21 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 17:55:21 GMT
WORKDIR /root
# Wed, 15 Apr 2026 17:56:06 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=64567d16674aa558a059d3c1af2dcde5fe222e166d092b11a721285d41361679;             SDK_ARCH="x64";;         armhf)             DART_SHA256=df9611c016da694f1d36dd923fc392bb1d5f9b3b5b8bf93d2367afdeb8522908;             SDK_ARCH="arm";;         arm64)             DART_SHA256=e211c35ce943eea9f2038c0ef351bad325ba959d7c58cf4e77f6eacc02389459;             SDK_ARCH="arm64";;         riscv64)             DART_SHA256=a0b2e7509e369ffb8f531526f7fb60003fda4bbee0da938fafa282d5c6e78c53;             SDK_ARCH="riscv64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.12.0-327.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5b5825255a5d4ee29acec2738aa43805937d5cf188e73592372b8d8cd778f`  
		Last Modified: Wed, 15 Apr 2026 18:00:44 GMT  
		Size: 44.2 MB (44183572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba610148dc501ed1a6c0cc789285e829e79332eb3ddd25d785e76a09e6cd77b`  
		Last Modified: Wed, 15 Apr 2026 18:00:28 GMT  
		Size: 1.6 MB (1564396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2a91fd004f5730e04f28e3f19160543f5342a0e99410bdc189d9c65fb41c95`  
		Last Modified: Wed, 15 Apr 2026 18:01:00 GMT  
		Size: 176.9 MB (176916916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta-sdk` - unknown; unknown

```console
$ docker pull dart@sha256:8393688d7ac3395727e60174421289ec1108ee287c6ada016fe293f3805cb6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 KB (18971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac945532d73e38fa6e58772ac4cb9a7baf47991fec39577c1451486ff65e08f7`

```dockerfile
```

-	Layers:
	-	`sha256:3809ff7bb5df0f204db71804d6c735e90225e68b0ee3aa216b98a69c081c1daa`  
		Last Modified: Wed, 15 Apr 2026 18:00:28 GMT  
		Size: 19.0 KB (18971 bytes)  
		MIME: application/vnd.in-toto+json
