## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:a025c1e2e7a52e3169d23f1cebea3e5670243149527fee7be160778cdb63f886
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:df21871e938ff96b7e17da95b8c051200b3b12db4c614a6bd7df035dcedfcc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12784523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770f61713e5e80316ae2d5b0ae85435afae0d5294e1a417dff4832b0603424a1`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 03 Feb 2025 02:59:38 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bae14b70df6a5152ffb6aa4f7db219a6b31a04aa96c0fbc6421213466fe505d`  
		Last Modified: Sat, 15 Feb 2025 09:24:37 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8468965d14c3b5811f6b6f22414aa4006bb76530265b4a0a44ed68b354f198c4`  
		Last Modified: Sat, 15 Feb 2025 09:24:37 GMT  
		Size: 1.1 MB (1116796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a9e07b1c45a05b5327ed544bcb134f13487561af7f708adb3debda5f26d7a`  
		Last Modified: Sat, 15 Feb 2025 09:24:38 GMT  
		Size: 8.0 MB (8021402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab65ae290d1c04dcfaacc2f5b9d6489bb5e2c49ed4ad7bd47717c5bf21b0bba2`  
		Last Modified: Sat, 15 Feb 2025 09:24:39 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7901c06000f20bd5c8fefe056f5364b2e8ec3293d9be7e0b3790c2ba6b95bf28`  
		Last Modified: Sat, 15 Feb 2025 09:24:39 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:609bbba498e08372a6d79197b054a03f8e92457a4a855ac160e4a0d0766752ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 KB (158002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4afd7a77190261d214db38069c0b1932df8fe8007f144e026192b7f822064de`

```dockerfile
```

-	Layers:
	-	`sha256:f3dabbfb5ca1f071c47d3f635a972252e30b351ce291d5f31f8204bf669bb29d`  
		Last Modified: Fri, 14 Feb 2025 21:30:38 GMT  
		Size: 140.9 KB (140913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb4392449a57d73079aefb57d7332503d11c9402c4d6af7c4804986d8041866`  
		Last Modified: Fri, 14 Feb 2025 21:30:39 GMT  
		Size: 17.1 KB (17089 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:588903ec0d76b47ed168cb07c7f61af5e107cab666f6d9b296f6caed7c81ded5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12337800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539d5243968d0790b3f8ce68296eaf47468b5b5117a1820ec208a2a45647d5e5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 03 Feb 2025 02:59:38 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243d2dc41e14c344d1a9f1cc74006025de32e9c01ef2676491ffb84c79f06b47`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb9be78d7b5d67e744c97d659dd70efb8bdf1a929307d78e18e5a313cb0333`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 1.1 MB (1129837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4180789d704a7ef80504849bf9c83b2971b6908782bfb14dcc5f488e0e67ad24`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 7.8 MB (7839162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7675f0103f9c23aa055cd3ad661db2e2ffaff1be9f89f2c5a40f01b048c19b`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111a52f8e59611672091fd46afb7f5c39eff2e929cca6dc3b0aa7bff5a5a1cd`  
		Last Modified: Fri, 14 Feb 2025 21:30:47 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:71f90bc44a6ee8c3667e23c0a9c59706e3ddd5344c59ea566e908a1b4d7cbfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20356f547d35628121e5070f13f79f4cac5a7f28f037af15c4aa1bb7383fcf5`

```dockerfile
```

-	Layers:
	-	`sha256:be5f9b3292abb44c643b1572249e55c45ece24fc3c8ab07e9cca14aa4db7ecfa`  
		Last Modified: Fri, 14 Feb 2025 21:30:40 GMT  
		Size: 17.0 KB (16954 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:edca286b7eeca981b0c6712bf0b88751668801c23ce50e0808a5d8ffe3895b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13235872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2090c62b3a579a8265d6361edc8154f92b6f0763e0dc014efecc85f9904e04b8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 03 Feb 2025 02:59:38 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["/bin/sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 03 Feb 2025 02:59:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Mon, 03 Feb 2025 02:59:38 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Mon, 03 Feb 2025 02:59:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENV NICK=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV SERVER=
# Mon, 03 Feb 2025 02:59:38 GMT
ENV LISTEN=3333
# Mon, 03 Feb 2025 02:59:38 GMT
ENV USERFILE=eggdrop.user
# Mon, 03 Feb 2025 02:59:38 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 03 Feb 2025 02:59:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 03 Feb 2025 02:59:38 GMT
EXPOSE map[3333/tcp:{}]
# Mon, 03 Feb 2025 02:59:38 GMT
COPY entrypoint.sh ./ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Mon, 03 Feb 2025 02:59:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 03 Feb 2025 02:59:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f437ca58399a638057c62b2fec6ea27022c6ba14ca6b1e748e425dd004369d77`  
		Last Modified: Sun, 16 Feb 2025 17:21:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ff23854b2cb7cc2af9ed9376082ad4ed0c2ffc31b68afedaea46db187d56c`  
		Last Modified: Sun, 16 Feb 2025 17:21:21 GMT  
		Size: 1.2 MB (1171028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958816378edfde5f40f73c6751957a2add2a47d5aced7436d57df71e6e356071`  
		Last Modified: Sun, 16 Feb 2025 17:21:22 GMT  
		Size: 8.1 MB (8067741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37103dd71102c1a0e5547fae2b66c5c50d5b2ca80e2fbfce46a4fdfdd5ac5643`  
		Last Modified: Sun, 16 Feb 2025 17:21:25 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8f56221f305640dc31f7b757db907f0d30c46c55af6451444bc6ffeb233b3b`  
		Last Modified: Sun, 16 Feb 2025 17:21:24 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:eea327f80f4be3a4bd0b35dbedac5a7e2df6b2e5fa651bc34bdb8215b986fa10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 KB (158122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7406f597f7c0749d07ab19b48840cdbb48e24db7f9e5a6f2bd6ae0cc50b2f2bf`

```dockerfile
```

-	Layers:
	-	`sha256:e07183601e9166b79501dc9273163739b8c5d6e7b176e262f4613e4fe9167d1a`  
		Last Modified: Sat, 15 Feb 2025 00:30:57 GMT  
		Size: 140.9 KB (140933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7377e263547758e2047849e5452a8ac7c7be7aefd3bdb7fa45657ebf66708b`  
		Last Modified: Sat, 15 Feb 2025 00:30:57 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json
