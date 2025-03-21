## `dart:beta`

```console
$ docker pull dart@sha256:2aafd466358f5a1fd72253d6303fa18c893aae103934603b4d999b8a7c387e60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:848c833e6e72c9c13fd5778623035ba23bad4ccf2add1533ee1ab2633659af69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297123553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484e0968e739858b9a582acf48f5958ca8e37a96b7ba57ccd2ddcfc5fedd36ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Mar 2025 13:36:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Mar 2025 13:36:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 13:36:12 GMT
WORKDIR /root
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6478773aa70f9868bf8e3965e635b820e8542ff4857f58c64eb68a4a860768f9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a7e92421770478ca74eb35df08ed25e0e0b0a22d6dcddd7dae6480bb1a67e1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=39784695c5686fecbe0391a84a41e8424f94602f72ceea0196da22065f274e70;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab54faae6114fbb7aae779cc63def1e7cc5bbd836126a80a0ac6c2232627a60`  
		Last Modified: Fri, 21 Mar 2025 16:30:09 GMT  
		Size: 54.9 MB (54907944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ef59740d7351ba78ab987eaa041de25ae7d53dcbf4c41102125104e9d43b10`  
		Last Modified: Fri, 21 Mar 2025 16:30:09 GMT  
		Size: 1.8 MB (1785445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b994ed2fe9e1af8de68cae6b74dc0b04e4c46ce62c75e9a7b3466932c2cd252e`  
		Last Modified: Fri, 21 Mar 2025 16:30:12 GMT  
		Size: 212.2 MB (212225267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:ab1ac2e549bc278edd7461415b570650f0d7e6e88ded89cfac6dc1f165d66667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450abbb25d6b204e775a1379af2969f4301e58e53bc98b1110fa588760dc0291`

```dockerfile
```

-	Layers:
	-	`sha256:b08354403a595a61c9d86bc2abf37c1a5cbb481c081d630868a8d742506744c0`  
		Last Modified: Fri, 21 Mar 2025 16:30:09 GMT  
		Size: 17.9 KB (17911 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm variant v7

```console
$ docker pull dart@sha256:e596798a76319df573989453c9f645d1bac455722141f6a94b61082f67092cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222219456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17acb4ed9520d2dfa03b51191b096bbc8f8859ee7a7e4bb81d3c2d0c8a6b78ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Mar 2025 13:36:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Mar 2025 13:36:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 13:36:12 GMT
WORKDIR /root
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6478773aa70f9868bf8e3965e635b820e8542ff4857f58c64eb68a4a860768f9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a7e92421770478ca74eb35df08ed25e0e0b0a22d6dcddd7dae6480bb1a67e1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=39784695c5686fecbe0391a84a41e8424f94602f72ceea0196da22065f274e70;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972839da75c60274dbfb6b7a02ff7ed1cb5db755f8e9b8242d787510a30fdc44`  
		Last Modified: Fri, 21 Mar 2025 16:29:59 GMT  
		Size: 49.6 MB (49562134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ce12a38521920d24bf7ce26f38e42745cfc4605890b8396fa5a739b9cacde5`  
		Last Modified: Fri, 21 Mar 2025 16:29:58 GMT  
		Size: 1.2 MB (1221939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c619d6fd922df271045afb3cfbedff55fe599fdfe53c0a728c9d3be184aa1b`  
		Last Modified: Fri, 21 Mar 2025 16:30:02 GMT  
		Size: 147.5 MB (147520263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:78a3a1d65e905a1a6148a2a7dea988ed94c08a6a07460a3287c5657ada4a7f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca87b56c7f49f17da8a9ada702bd750d54cadfa5bdf62c63e4df74ac1504d1`

```dockerfile
```

-	Layers:
	-	`sha256:dd5ac451a26c716836af029956cad70b7698dad7bb7873fd20b8b5915e32c9e3`  
		Last Modified: Fri, 21 Mar 2025 16:29:58 GMT  
		Size: 18.0 KB (18013 bytes)  
		MIME: application/vnd.in-toto+json

### `dart:beta` - linux; arm64 variant v8

```console
$ docker pull dart@sha256:34224c252e6829d97de51eef6a26150f7d6a1b3eb4a06661a57874a09a19cf10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295679135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22354003ed5ab75920294de41ec205d3b01cf555d9010797148d5012549cd8d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             TRIPLET="x86_64-linux-gnu" ;             FILES="/lib64/ld-linux-x86-64.so.2" ;;         armhf)             TRIPLET="arm-linux-gnueabihf" ;             FILES="/lib/ld-linux-armhf.so.3                 /lib/arm-linux-gnueabihf/ld-linux-armhf.so.3";;         arm64)             TRIPLET="aarch64-linux-gnu" ;             FILES="/lib/ld-linux-aarch64.so.1                 /lib/aarch64-linux-gnu/ld-linux-aarch64.so.1" ;;         *)             echo "Unsupported architecture" ;             exit 5;;     esac;     FILES="$FILES         /etc/nsswitch.conf         /etc/ssl/certs         /usr/share/ca-certificates         /lib/$TRIPLET/libc.so.6         /lib/$TRIPLET/libdl.so.2         /lib/$TRIPLET/libm.so.6         /lib/$TRIPLET/libnss_dns.so.2         /lib/$TRIPLET/libpthread.so.0         /lib/$TRIPLET/libresolv.so.2         /lib/$TRIPLET/librt.so.1";     for f in $FILES; do         dir=$(dirname "$f");         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done # buildkit
# Tue, 18 Mar 2025 13:36:12 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 18 Mar 2025 13:36:12 GMT
ENV PATH=/usr/lib/dart/bin:/root/.pub-cache/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Mar 2025 13:36:12 GMT
WORKDIR /root
# Tue, 18 Mar 2025 13:36:12 GMT
RUN set -eux;     case "$(dpkg --print-architecture)" in         amd64)             DART_SHA256=6478773aa70f9868bf8e3965e635b820e8542ff4857f58c64eb68a4a860768f9;             SDK_ARCH="x64";;         armhf)             DART_SHA256=3a7e92421770478ca74eb35df08ed25e0e0b0a22d6dcddd7dae6480bb1a67e1d;             SDK_ARCH="arm";;         arm64)             DART_SHA256=39784695c5686fecbe0391a84a41e8424f94602f72ceea0196da22065f274e70;             SDK_ARCH="arm64";;     esac;     SDK="dartsdk-linux-${SDK_ARCH}-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/3.8.0-171.1.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "$DART_SHA256 *$SDK"         | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK"         && chmod 755 "$DART_SDK" && chmod 755 "$DART_SDK/bin"; # buildkit
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32755a8c482c5957377edd0359515c90b3ab6877648bd68e704eae93b506b29`  
		Last Modified: Fri, 21 Mar 2025 16:29:53 GMT  
		Size: 54.7 MB (54678836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5046a43de9771a0c085cd2b738532f25eab41aeefe6220024b49e25fc0bd8fce`  
		Last Modified: Fri, 21 Mar 2025 16:29:51 GMT  
		Size: 1.5 MB (1488212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff24647b8dbb052f863887ef0440e8aef58a6de657b8c4f157eeb6dba5789475`  
		Last Modified: Fri, 21 Mar 2025 16:29:56 GMT  
		Size: 211.5 MB (211468018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `dart:beta` - unknown; unknown

```console
$ docker pull dart@sha256:390ef4fe4c1ba7451257970381721ac8567678262149545021dd69f6135a7baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a2437120ea5dc6f9ad3686e3e751db0687685553e90a86ae5af54737aa75b0`

```dockerfile
```

-	Layers:
	-	`sha256:916d7aa566165c76944db6ecda8ee150bbd04d2b2cf35988faaef4f70082498e`  
		Last Modified: Fri, 21 Mar 2025 16:29:51 GMT  
		Size: 18.0 KB (18045 bytes)  
		MIME: application/vnd.in-toto+json
