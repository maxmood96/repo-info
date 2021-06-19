## `dart:beta-sdk`

```console
$ docker pull dart@sha256:1f8f89cfdd15f38445883485edea6d1740a1a788ab612091f46d5472e6295297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `dart:beta-sdk` - linux; amd64

```console
$ docker pull dart@sha256:658fc4815b0049e19db2b0d3da892d5671a1c46da5e9909c4661626fbfca17c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288896872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74580fef0f029b8bc2b53c056d0f25d0a7950e7caa05548a81e666336ac0c718`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Thu, 10 Jun 2021 18:21:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Thu, 10 Jun 2021 18:21:31 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Thu, 10 Jun 2021 18:21:31 GMT
ENV DART_SDK=/usr/lib/dart
# Thu, 10 Jun 2021 18:21:32 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 10 Jun 2021 18:21:32 GMT
WORKDIR /root
# Fri, 18 Jun 2021 18:20:54 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.14.0-188.3.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "caeb5a18e7e309096d07755d3abb8398024995e133e19cc55109679abd11376d *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659f65799b4f9a55a6ab63d14c0a8e07ed9663ccd04cd900e633473030146a10`  
		Last Modified: Thu, 10 Jun 2021 18:22:15 GMT  
		Size: 49.6 MB (49580179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f02b7fed81642e9e345e6271782e691d4cf743ff496200c5a814118976884b`  
		Last Modified: Thu, 10 Jun 2021 18:22:07 GMT  
		Size: 2.4 MB (2359151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ddacfa206e2eb337cf6c4e2b167502082719b6dbcb409100de9df64d7e9d6d`  
		Last Modified: Fri, 18 Jun 2021 18:21:51 GMT  
		Size: 209.8 MB (209811627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
