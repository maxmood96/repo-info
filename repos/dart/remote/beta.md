## `dart:beta`

```console
$ docker pull dart@sha256:20c8f5ea4a8e51dd3844428679de971e9b6c2d9a078e2347ffdb6b55f487d6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:21fb1085ba28aafab3523a05872dbe84859e2c2db05221114d1cf1d0d3cc17d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248829305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfa5b58d88747e092aba5d92fd099d49e7ffad072ef41c1ccb1217fb51ae697`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Mon, 17 May 2021 20:18:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         openssh-client         unzip         dnsutils     ;     rm -rf /var/lib/apt/lists/*
# Mon, 17 May 2021 20:18:55 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Mon, 17 May 2021 20:18:55 GMT
ENV DART_SDK=/usr/lib/dart
# Mon, 17 May 2021 20:18:55 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 May 2021 20:18:56 GMT
WORKDIR /root
# Mon, 17 May 2021 20:19:25 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     DART_VERSION=2.13.0-211.14.beta;     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/$DART_VERSION/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "d33e7727eb3e49fda8c854a4aa894e642b1b760e0bf68ca382778f30242904c2 *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef6b6cb7d8e58573bab3165075efc383447aaf34b4eff54c220f0ee5b55206f`  
		Last Modified: Mon, 17 May 2021 20:19:57 GMT  
		Size: 23.7 MB (23682897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4bafd8baa9cbcae1f326916610f19c163a88d49af4205c08859fd4631e9a75`  
		Last Modified: Mon, 17 May 2021 20:19:53 GMT  
		Size: 2.4 MB (2359133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e5145a6f2f8399a5c918b67758ae161cd153e9e1935f625744ce137ae7fba`  
		Last Modified: Mon, 17 May 2021 20:21:20 GMT  
		Size: 195.6 MB (195641360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
