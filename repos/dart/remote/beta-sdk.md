## `dart:beta-sdk`

```console
$ docker pull dart@sha256:cc15aaa9371619c834d99a87c1732806ad0adacd2d3c7178b17d3d2f41d09841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:7ebdbc2120057173b3767d45e4ca8ff72734e044c11f96307a7b538f20147387
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275793611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524bcbb3be31fdd84669eba0170cf697a7484702c3b41de935ac6609c7d59ad6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:13:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:13:38 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 20 Apr 2022 07:13:38 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Apr 2022 07:13:38 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 07:13:38 GMT
WORKDIR /root
# Thu, 21 Apr 2022 11:42:53 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=dc3123d87c1b6b43087520ba9fa7e6fd91f3c4652178d55ca41825f4fc7100fe;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3b825fa4c6bdd7809185d9acbe4e7030900ea0edd14c17aa6255d7665910e9a1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6c0f0777241fb8b2d0607295f794956b9a91d3251f639c32fd351902dfae931;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-266.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1caab2cc88d2bfef34fc56a9f094f5065d8b9ac996e4afeaa664e4484f75f65`  
		Last Modified: Wed, 20 Apr 2022 07:14:35 GMT  
		Size: 45.1 MB (45072693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c033219b7813c4cd899bc0748dcfac42c25d78a696fd5da94eeda7ef1dd8562`  
		Last Modified: Wed, 20 Apr 2022 07:14:28 GMT  
		Size: 2.1 MB (2139552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30469deefea52624592ef014074ad2dd65b8a382ead07736bc5011ac26d5601`  
		Last Modified: Thu, 21 Apr 2022 11:43:43 GMT  
		Size: 197.2 MB (197202387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm variant v7

```console
$ docker pull dart@sha256:6727a046920472dec2502644706ce973a6b2d5cbd716a554b6c6ce85f1750bc6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184077668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d877f0e105911d51948b657ed7beed93c71debe85a4ac1018a4ba1364368f3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 13:27:18 GMT
ADD file:1a0e290eb32b3533f9d1684c683ad866b5003579790b25ad61b2044dc6c20bbb in / 
# Wed, 20 Apr 2022 13:27:18 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 20:50:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 20:50:42 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 20 Apr 2022 20:50:43 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Apr 2022 20:50:43 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 20:50:44 GMT
WORKDIR /root
# Wed, 20 Apr 2022 20:51:43 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=afd52527908e2184301873ef2252e13ed3d9938d47acff26297b45376d165e51;             SDK_ARCH="x64";;         armhf)             DART_SHA256=b41216eb894471a3fa6646319f5def4fe7c5115d8be9b664754a7d02a9130c6b;             SDK_ARCH="arm";;         arm64)             DART_SHA256=3045035160b0af67111cd28aef5d8cbd50d264deb279d23e77767a0a2137a236;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-266.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:a6b2963233cd14b47391f0e25f2a485bbeabb87e771a71b73e5cde7c013963da`  
		Last Modified: Wed, 20 Apr 2022 13:43:41 GMT  
		Size: 26.6 MB (26575758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5128dd097d08ca6e030832d392aff57df592d503fd9f8927c4831056bd15eb9`  
		Last Modified: Wed, 20 Apr 2022 20:53:20 GMT  
		Size: 41.0 MB (40966671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d75d0f36fdc93d65e1d2abd95d63816ec15230b3c1702213f2f90899d89533`  
		Last Modified: Wed, 20 Apr 2022 20:52:57 GMT  
		Size: 1.3 MB (1288081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466b6bc3bb1fa9bf2e14ca0daf4ec7464ee4581ee40c18afc54d3b4ea4f9199`  
		Last Modified: Wed, 20 Apr 2022 20:56:13 GMT  
		Size: 115.2 MB (115247158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `dart:beta-sdk` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:71dfdffe7b69e1bfd2be6c678f1f2429c111b10c34b2e788afe5c57bd6916e73
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 MB (193148078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc544427d29b68af2c10a78adc79b3fb2052e39e3957bc5306ec0499d3e8c39`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:10 GMT
ADD file:84523b5820128293b713ef35d8db618921162250da1e4c72bf9923f34ad7d87d in / 
# Wed, 20 Apr 2022 04:29:11 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 07:06:55 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 07:06:56 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Wed, 20 Apr 2022 07:06:57 GMT
ENV DART_SDK=/usr/lib/dart
# Wed, 20 Apr 2022 07:06:58 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 07:06:59 GMT
WORKDIR /root
# Thu, 21 Apr 2022 13:35:22 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=dc3123d87c1b6b43087520ba9fa7e6fd91f3c4652178d55ca41825f4fc7100fe;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3b825fa4c6bdd7809185d9acbe4e7030900ea0edd14c17aa6255d7665910e9a1;             SDK_ARCH="arm";;         arm64)             DART_SHA256=f6c0f0777241fb8b2d0607295f794956b9a91d3251f639c32fd351902dfae931;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.17.0-266.5.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin";
```

-	Layers:
	-	`sha256:6d4a449ac69c579312443ded09f57c4894e7adb42f7406abd364f95982fafc59`  
		Last Modified: Wed, 20 Apr 2022 04:35:49 GMT  
		Size: 30.1 MB (30065801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5224c49f1d6ea5a648b1560bb384a0be9fc6ff3c7e310d18312405ade51d9e`  
		Last Modified: Wed, 20 Apr 2022 07:08:10 GMT  
		Size: 44.8 MB (44789156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be3f5b9fa7637985357830365527bb1813dbf5d63928ff1da2502af3f97c324`  
		Last Modified: Wed, 20 Apr 2022 07:08:03 GMT  
		Size: 1.6 MB (1556721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888ba7441581f9002c6dc8804e935b49301469161bde20d7dbb7faa5f35f5ca0`  
		Last Modified: Thu, 21 Apr 2022 13:36:18 GMT  
		Size: 116.7 MB (116736400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
