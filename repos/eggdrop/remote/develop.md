## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:e8c83128d677c66c04e550f88862309e20912169b10bd41126ab640ebaf9832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:6f2ec691a0024863785b04223faacc19f52ffe8becff48c989d11894a6589d67
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16408839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd366d9d4db778c379ea933e0e590d80630a8e001e76042f5b775e94741d5054`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 20:19:33 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 20:19:33 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 20:19:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 20:19:35 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 20:19:35 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 20:21:55 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 20:21:55 GMT
ENV NICK=
# Thu, 08 Aug 2024 20:21:55 GMT
ENV SERVER=
# Thu, 08 Aug 2024 20:21:55 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 20:21:55 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 20:21:55 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 20:21:55 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 20:21:55 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 20:21:55 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 20:21:56 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 20:21:56 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 20:21:56 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25cead120aee1bf7e0968221f9592609ba01caea492b28d7b4df5ba86aebf48c`  
		Last Modified: Thu, 08 Aug 2024 20:29:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd3b040bb37208218a0f2be38eb25e03dacef276a439cf900ab8631abbf4295`  
		Last Modified: Thu, 08 Aug 2024 20:29:07 GMT  
		Size: 1.1 MB (1115320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a21719a673bc7044f1a8936d37b8771e90c5f8114a49e402c0562a0d7e436ac`  
		Last Modified: Thu, 08 Aug 2024 20:29:08 GMT  
		Size: 11.7 MB (11666586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08904f4b13350999ac96fde726feed04df72deb0b57257adab0a97f610bf3935`  
		Last Modified: Thu, 08 Aug 2024 20:29:07 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e83dc96e9e2aca0e7710e0e24d6dacfd48b74131f8b0dd184c8adea540f8d`  
		Last Modified: Thu, 08 Aug 2024 20:29:07 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:f286c4877ad2d20067287ce7737eff999faaacd2b5f588b39762aa0eb6b43cfa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15979212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04801fecad6c737092d0126e52640454b7851bdd7d185f260f0be85fd49b53e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:51:31 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:51:33 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:51:35 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 19:51:35 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 19:51:36 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 19:54:50 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 19:54:50 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:54:51 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:54:51 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:54:51 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:54:51 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:54:51 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:54:51 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:54:51 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 19:54:51 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 19:54:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:54:52 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade96c498913dfb986e395fa5b382c7643627c76acf91dc28bfd94b61bfdbda1`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 967.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db39b8b10cbe820079ef063c33200dfba1b45391bc84208ff5290cfca48a06ed`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 1.1 MB (1129499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8b508fe0cf020d7ecc788220ea62cc0fa523c49656cc03cf25b55c88aefbcf`  
		Last Modified: Thu, 08 Aug 2024 20:02:49 GMT  
		Size: 11.5 MB (11480475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ce2f158695962f3c8d126daed3dc572fe2f2ed3204945d45160b830d010ba`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121ef4537f6329562260380c3b604f446f433e3219a4c446565041b45c5804db`  
		Last Modified: Thu, 08 Aug 2024 20:02:47 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1bde69ebc16112c43db8461ea3bc2cf30733f3eba70de7c41b33b5e1a03bee8c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17001287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e8ef8aaf5fbaf76e979d266a2e91750a75987f53ff256e440f1006fddad8e6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:43:37 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:43:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:43:39 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 19:43:39 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 19:43:39 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 19:45:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 19:45:35 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:45:35 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:45:35 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:45:35 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:45:36 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:45:36 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:45:36 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:45:36 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 19:45:36 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 19:45:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:45:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df1fbd90925124f99f470d0e8fb64bb807608c5c0bbe563414aaec386a6b0ca`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1131de528037c7182c2a886926b7114abcc3062bddced8c87d376e2afe96a63`  
		Last Modified: Thu, 08 Aug 2024 19:51:53 GMT  
		Size: 1.2 MB (1210745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbb79da626c1f3ac029f6f510202afe3435f1ad9e5dd1d6f6b18fa19486b1e7`  
		Last Modified: Thu, 08 Aug 2024 19:51:54 GMT  
		Size: 11.7 MB (11699558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfdcfdbffa5694231ca240b034fe2db03102fe20212c6622321f33a630af3b03`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 2.0 KB (1956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7806ead3de8a9b031855581e4f6c95dc82835fc6dce8e32eb5f07e9f3ceae506`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
