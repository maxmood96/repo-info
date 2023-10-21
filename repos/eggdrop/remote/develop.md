## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:e8c3570f7fd01826ff7c70b5c1fdad096217d79d59c9614cd5d157ba026227a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:9ec6b149a789433e2df240dce0dc83a36c33c82d50361683f7b1d0145331342a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18181286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4df521af73130bbe77b03bd8ecc6b8a34b79233f59eb491c1eadc2f4a50df0a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:17:09 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 21 Oct 2023 00:17:10 GMT
RUN adduser -S eggdrop
# Sat, 21 Oct 2023 00:17:11 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Oct 2023 00:17:11 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Sat, 21 Oct 2023 00:17:11 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Sat, 21 Oct 2023 00:17:12 GMT
RUN apk --update add --no-cache bash openssl
# Sat, 21 Oct 2023 00:20:47 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 21 Oct 2023 00:20:47 GMT
ENV NICK=
# Sat, 21 Oct 2023 00:20:47 GMT
ENV SERVER=
# Sat, 21 Oct 2023 00:20:47 GMT
ENV LISTEN=3333
# Sat, 21 Oct 2023 00:20:48 GMT
ENV OWNER=
# Sat, 21 Oct 2023 00:20:48 GMT
ENV USERFILE=eggdrop.user
# Sat, 21 Oct 2023 00:20:48 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 21 Oct 2023 00:20:48 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 21 Oct 2023 00:20:48 GMT
EXPOSE 3333
# Sat, 21 Oct 2023 00:20:48 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Sat, 21 Oct 2023 00:20:48 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 21 Oct 2023 00:20:48 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 21 Oct 2023 00:20:48 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5097e7c90940c1ad08f4c14384b6e2b7bab2641e3962c1d08ea52eed9ae3cd5a`  
		Last Modified: Sat, 21 Oct 2023 00:25:21 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6848297e98706c32911ba7521bbbcb939e30b344e80d82a4c23ae786c4bce2c`  
		Last Modified: Sat, 21 Oct 2023 00:25:19 GMT  
		Size: 11.0 KB (10989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a7878a3e855d542a57210de1c56489094335eee11c07130b0fb1c43d9382d1`  
		Last Modified: Sat, 21 Oct 2023 00:25:19 GMT  
		Size: 3.3 MB (3252168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c554af8b3fe3416653bd54e0be76715af3815378bc526f99d99db471dcc56eab`  
		Last Modified: Sat, 21 Oct 2023 00:25:21 GMT  
		Size: 11.5 MB (11535291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcad910f3e97b3929931557c9fc1dd692de3dc7a35634dae4b16a1dcd47ad663`  
		Last Modified: Sat, 21 Oct 2023 00:25:19 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd80a7788f9c59b9fbbfe008475855d8ea16bf7def77b49ffcd90b07b9de35ca`  
		Last Modified: Sat, 21 Oct 2023 00:25:19 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:30a7a308cfcea1ea1bc576923eb8ff8c748da96d4828d2115ad1ccae79c63d88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3251e9d7fd1d6b3b8b388434101b61ebd453051325ac4f1b73caae918b3f6e1e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:17 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Mon, 07 Aug 2023 19:49:18 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:10:47 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 21 Oct 2023 00:10:47 GMT
RUN adduser -S eggdrop
# Sat, 21 Oct 2023 00:10:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Oct 2023 00:10:49 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Sat, 21 Oct 2023 00:10:49 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Sat, 21 Oct 2023 00:10:50 GMT
RUN apk --update add --no-cache bash openssl
# Sat, 21 Oct 2023 00:14:50 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 21 Oct 2023 00:14:50 GMT
ENV NICK=
# Sat, 21 Oct 2023 00:14:50 GMT
ENV SERVER=
# Sat, 21 Oct 2023 00:14:51 GMT
ENV LISTEN=3333
# Sat, 21 Oct 2023 00:14:51 GMT
ENV OWNER=
# Sat, 21 Oct 2023 00:14:51 GMT
ENV USERFILE=eggdrop.user
# Sat, 21 Oct 2023 00:14:51 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 21 Oct 2023 00:14:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 21 Oct 2023 00:14:51 GMT
EXPOSE 3333
# Sat, 21 Oct 2023 00:14:51 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Sat, 21 Oct 2023 00:14:51 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 21 Oct 2023 00:14:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 21 Oct 2023 00:14:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4ec6262b62e41d8a8f8e52845f045e8f5423bda0992f043a13948852ca7901`  
		Last Modified: Sat, 21 Oct 2023 00:19:44 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57be97f6f3da285f2b2d73fc8e6414c7c22b8c5992b5b44210da98fb0a54ddf4`  
		Last Modified: Sat, 21 Oct 2023 00:19:42 GMT  
		Size: 11.1 KB (11135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf499a5e20f059db7a7b11fb294d0680faaeef1ffbfa658104944022afb2bf6`  
		Last Modified: Sat, 21 Oct 2023 00:19:43 GMT  
		Size: 2.9 MB (2908328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99a8d1abef82936ac3a64d82137120b89d32d276a02805f504813d5d17061b8`  
		Last Modified: Sat, 21 Oct 2023 00:19:45 GMT  
		Size: 11.4 MB (11416260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee03e622047ae729fe2eab736833104ab858db8c1c43755b6ac5860992117fb`  
		Last Modified: Sat, 21 Oct 2023 00:19:42 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32772a93cf6aefda6bb0f35cd0a295b7cfa7cc85e25cfc035670205fe1ac6ad3`  
		Last Modified: Sat, 21 Oct 2023 00:19:42 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:434723b4a32a107b6c46255d6baac14ea5ac686e035bde0a90a5ede47d32c45b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17999216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f44acc245648a017b91609c358e0a36b668ebbc166fb9003b69f8094ffdf4c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:27:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 21 Oct 2023 00:27:00 GMT
RUN adduser -S eggdrop
# Sat, 21 Oct 2023 00:27:01 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 21 Oct 2023 00:27:01 GMT
ENV EGGDROP_SHA256=cc7936ee427959081651319119ac0b8f3581a18d7be7b20f71023954f1f69a91
# Sat, 21 Oct 2023 00:27:02 GMT
ENV EGGDROP_COMMIT=26ecf0921ee84c5bf61cb31014a75f02670b1af4
# Sat, 21 Oct 2023 00:27:03 GMT
RUN apk --update add --no-cache bash openssl
# Sat, 21 Oct 2023 00:30:16 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 21 Oct 2023 00:30:16 GMT
ENV NICK=
# Sat, 21 Oct 2023 00:30:16 GMT
ENV SERVER=
# Sat, 21 Oct 2023 00:30:16 GMT
ENV LISTEN=3333
# Sat, 21 Oct 2023 00:30:16 GMT
ENV OWNER=
# Sat, 21 Oct 2023 00:30:17 GMT
ENV USERFILE=eggdrop.user
# Sat, 21 Oct 2023 00:30:17 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 21 Oct 2023 00:30:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 21 Oct 2023 00:30:17 GMT
EXPOSE 3333
# Sat, 21 Oct 2023 00:30:17 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Sat, 21 Oct 2023 00:30:17 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 21 Oct 2023 00:30:17 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 21 Oct 2023 00:30:17 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a2ced791972b216815dd42fd739c68f0680a3ed1a67387c2b8283c13c85dff`  
		Last Modified: Sat, 21 Oct 2023 00:34:26 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b568cceab414e981235856af6f65ffe7ee2700aae2472603fb44c121a9ab7f6d`  
		Last Modified: Sat, 21 Oct 2023 00:34:24 GMT  
		Size: 11.2 KB (11197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f351ab106c115180f7491baa4ca79c6ee60b864f63a7439ed3629bb2cefde6b`  
		Last Modified: Sat, 21 Oct 2023 00:34:24 GMT  
		Size: 3.1 MB (3132455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a00efa51ec343ea1113bc4c62668ff6670bb32327f94d8de6ad745d31de419`  
		Last Modified: Sat, 21 Oct 2023 00:34:25 GMT  
		Size: 11.6 MB (11593048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24544ac82c2409e45ee2b80011b14959f0da2187c95b93e8fe0eb70c644dd0d1`  
		Last Modified: Sat, 21 Oct 2023 00:34:23 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fcf9b2acdfc3f8526d71fb3aca4806e1c0ed463bbe2deed3e704c0fe7b78ac`  
		Last Modified: Sat, 21 Oct 2023 00:34:24 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
