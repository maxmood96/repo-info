## `dart:beta`

```console
$ docker pull dart@sha256:a02540f84687a3899657e40693ec8456a5874465c25d7dc233032375424789a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `dart:beta` - linux; amd64

```console
$ docker pull dart@sha256:31a73ba255005e23039577515847d287c0425bb0e96a96e26cfdd05e8b2f83ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.0 MB (288976314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939c668fe458e6db497466a49092fa7522bc4c80754717f68908b7b5c205a232`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:29:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         curl         dnsutils         git         openssh-client         unzip     ;     rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 10:29:23 GMT
RUN set -eux;     for f in         /etc/nsswitch.conf         /etc/ssl/certs         /lib/x86_64-linux-gnu/libc.so.6         /lib/x86_64-linux-gnu/libdl.so.2         /lib/x86_64-linux-gnu/libm.so.6         /lib/x86_64-linux-gnu/libnss_dns.so.2         /lib/x86_64-linux-gnu/libpthread.so.0         /lib/x86_64-linux-gnu/libresolv.so.2         /lib/x86_64-linux-gnu/librt.so.1         /lib64/ld-linux-x86-64.so.2         /usr/share/ca-certificates     ; do         dir="$(dirname "$f")";         mkdir -p "/runtime$dir";         cp --archive --link --dereference --no-target-directory "$f" "/runtime$f";     done
# Tue, 17 Aug 2021 10:29:24 GMT
ENV DART_SDK=/usr/lib/dart
# Tue, 17 Aug 2021 10:29:24 GMT
ENV PATH=/usr/lib/dart/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 10:29:24 GMT
WORKDIR /root
# Thu, 19 Aug 2021 20:19:52 GMT
RUN set -eux;     ARCH=$(case "$(dpkg --print-architecture)" in amd64) echo "x64";; esac;);     SDK="dartsdk-linux-$ARCH-release.zip";     BASEURL="https://storage.googleapis.com/dart-archive/channels";     URL="$BASEURL/beta/release/2.14.0-377.7.beta/sdk/$SDK";     echo "SDK: $URL" >> dart_setup.log ;     curl -fLO "$URL";     echo "331004e674ebc9bdd4bb91b238fbd0190fcaae0e9205c8d85e6257ef60d4fabf *$SDK"     | sha256sum --check --status --strict -;     unzip "$SDK" && mv dart-sdk "$DART_SDK" && rm "$SDK";
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf70384699785586e7ce2387dcc48a39b1fa8b9837b6ec033441a3dd93ce4818`  
		Last Modified: Tue, 17 Aug 2021 10:30:35 GMT  
		Size: 49.6 MB (49581314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4c0190f1231c9d6c5fbfffaca9ee1baff80d891a3c91988c9bd7de914f9fd6`  
		Last Modified: Tue, 17 Aug 2021 10:30:21 GMT  
		Size: 2.4 MB (2359146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fde83de3ac316252851ece021a0d329d1fafabf887bed0ac5b34318e2a5016b`  
		Last Modified: Thu, 19 Aug 2021 20:20:48 GMT  
		Size: 209.9 MB (209889869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
