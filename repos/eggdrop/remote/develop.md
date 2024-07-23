## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:338ae1adc6467155e90e25f3797c26f5103cdc64791a5f48e2f90625f77c0e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:2f36a7f7c26559179d3bea4814207667f99797a14c8ed0f06565e2244753ae4f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16104405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a612b2e1157682c0bc7a87919745faed530abefaa04adb4f88d6a2739c6a256f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Wed, 26 Jun 2024 16:51:05 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 26 Jun 2024 16:51:06 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Wed, 26 Jun 2024 16:51:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Wed, 26 Jun 2024 16:51:07 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Wed, 26 Jun 2024 16:51:07 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Wed, 26 Jun 2024 16:53:37 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Wed, 26 Jun 2024 16:53:37 GMT
ENV NICK=
# Wed, 26 Jun 2024 16:53:37 GMT
ENV SERVER=
# Wed, 26 Jun 2024 16:53:37 GMT
ENV LISTEN=3333
# Wed, 26 Jun 2024 16:53:37 GMT
ENV USERFILE=eggdrop.user
# Wed, 26 Jun 2024 16:53:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 26 Jun 2024 16:53:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 26 Jun 2024 16:53:38 GMT
EXPOSE 3333
# Wed, 26 Jun 2024 16:53:38 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Wed, 26 Jun 2024 16:53:38 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Wed, 26 Jun 2024 16:53:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 26 Jun 2024 16:53:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e5cf294e09fd7f4effe5cff0c57a211f41aaee778ec6715750ac0c487107b3`  
		Last Modified: Wed, 26 Jun 2024 16:53:53 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e22a2e4f1c3c5db4af9dcd1caf769ae766cb7332ac61820c8ccf3ee07d4a537`  
		Last Modified: Wed, 26 Jun 2024 16:53:54 GMT  
		Size: 1.1 MB (1093051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1301de2282ecd4f73f7d4824169c9a3fbf390367d214c8b7c08b19ca720c7262`  
		Last Modified: Wed, 26 Jun 2024 16:53:55 GMT  
		Size: 11.6 MB (11589693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d502b23edb843965c5408a88dc3d3be7abb0b32367ea032d6453ff9b33be7e`  
		Last Modified: Wed, 26 Jun 2024 16:53:53 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e486719c62d7526c8e13756a7207658a4ddf19438f0c72139825798c25c942f`  
		Last Modified: Wed, 26 Jun 2024 16:53:53 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:62e39f5afa5f010a841aa895f21e6a94bc6f62d941d0270add0a744286ab0817
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15750081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1df737261c7cab5c1ca10160b88da52beee45d6c9fe649213a10b0a2813719a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:07:08 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 22 Jul 2024 22:07:09 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 22 Jul 2024 22:07:10 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 22 Jul 2024 22:07:10 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 22 Jul 2024 22:07:10 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 22 Jul 2024 22:09:59 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 22 Jul 2024 22:09:59 GMT
ENV NICK=
# Mon, 22 Jul 2024 22:09:59 GMT
ENV SERVER=
# Mon, 22 Jul 2024 22:09:59 GMT
ENV LISTEN=3333
# Mon, 22 Jul 2024 22:09:59 GMT
ENV USERFILE=eggdrop.user
# Mon, 22 Jul 2024 22:09:59 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 22 Jul 2024 22:09:59 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 22 Jul 2024 22:10:00 GMT
EXPOSE 3333
# Mon, 22 Jul 2024 22:10:00 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 22 Jul 2024 22:10:00 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 22 Jul 2024 22:10:00 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 22 Jul 2024 22:10:00 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0eaf2fcada43d50bf6c0923dffc862babcfc69356c5a9f726d722c0eaca50f`  
		Last Modified: Mon, 22 Jul 2024 22:10:25 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6564c02977f47d6f55bf958d52a49b9716a9e4c0be221ea00279f21c81e2d2ee`  
		Last Modified: Mon, 22 Jul 2024 22:10:26 GMT  
		Size: 1.1 MB (1106443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f7e0d985ff08eddd44a0d2eabe66d91a6a91c4ec27fc6181de07e4fa47dabe`  
		Last Modified: Mon, 22 Jul 2024 22:10:28 GMT  
		Size: 11.5 MB (11463644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4af96d901acf0b3ac30c06259ed5cb83cbd9c787c347a2374b858e78fea33b`  
		Last Modified: Mon, 22 Jul 2024 22:10:25 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4bd9c8e395b45e20b0eccc9420513a689028a79c29433d9c86b305461ead8`  
		Last Modified: Mon, 22 Jul 2024 22:10:25 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:200065653dc156a9d5fb0ee595df3f381a0962c0819e303b51587d0ab41a0fc8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16228840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320eed47c641f27b8cfdfaae365ac638e271bf7b5d1f6a1dc14feb1c18ed7009`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:13:42 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Mon, 22 Jul 2024 22:13:43 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Mon, 22 Jul 2024 22:13:44 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Mon, 22 Jul 2024 22:13:44 GMT
ENV EGGDROP_SHA256=a46bf0e77ed2af907fe6e15b77bddf0c55706258070a05c92810e0bd40a1fe3b
# Mon, 22 Jul 2024 22:13:44 GMT
ENV EGGDROP_COMMIT=4703f71067437c361ca8d5c8c4a09d41561a7a20
# Mon, 22 Jul 2024 22:15:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Mon, 22 Jul 2024 22:15:43 GMT
ENV NICK=
# Mon, 22 Jul 2024 22:15:43 GMT
ENV SERVER=
# Mon, 22 Jul 2024 22:15:43 GMT
ENV LISTEN=3333
# Mon, 22 Jul 2024 22:15:43 GMT
ENV USERFILE=eggdrop.user
# Mon, 22 Jul 2024 22:15:43 GMT
ENV CHANFILE=eggdrop.chan
# Mon, 22 Jul 2024 22:15:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Mon, 22 Jul 2024 22:15:44 GMT
EXPOSE 3333
# Mon, 22 Jul 2024 22:15:44 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Mon, 22 Jul 2024 22:15:44 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Mon, 22 Jul 2024 22:15:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Mon, 22 Jul 2024 22:15:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf4e7f932520793ddc42e6a32b7fd015e33cac54d4988e8b0d04b2379da8df1`  
		Last Modified: Mon, 22 Jul 2024 22:15:57 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14983e0432148b2f5db656835f7d4b91a4e41def97262f8f51bb9fc18609770d`  
		Last Modified: Mon, 22 Jul 2024 22:15:58 GMT  
		Size: 1.2 MB (1188253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027c8dc929e8875f7100207b41e378e897e5502d50b296f0dd1a0f1f71176a1b`  
		Last Modified: Mon, 22 Jul 2024 22:15:59 GMT  
		Size: 11.7 MB (11677802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352a18ed83b6ff81e3b9a3b82381a21a35c2a7b6f62ab8e84cfb241d0c638a2f`  
		Last Modified: Mon, 22 Jul 2024 22:15:57 GMT  
		Size: 2.0 KB (1953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4589b6cb33c27311574a8fb69fb89df3051aa2b9afcaa4695ae908ddc79425f6`  
		Last Modified: Mon, 22 Jul 2024 22:15:57 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
