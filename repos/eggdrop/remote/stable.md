## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:c72039395517ace38f0954dfd415d41bf6a1beae75f3bd907898d0ef1a7ab9d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:464fa69cb45f5509980cd7b70bdf33209d893d95c3fd4e1a4cd6a2e1416564f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d06db72b6c7a18beee096a1b8fba98574219450ef740740bcce13e71ef7e771`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97044ed21665bdc39e4fb6615c274aed679f6b8f55e5465fae4f555719965f9b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687876d96a0d41fb3e048eac436131b2b6815643c88e7bd077811d7b63bddc04`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353807a5a9d0ab0b70534e9de509c882d3c03958adccae7962bab12d41a030f`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 2.9 MB (2900184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab05178db53ad0b2b8818dbb268a624880309ac9d286fc96d24df5b593b348b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 6.0 MB (5964265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102028674158922bccbfdcd6d7ea8994766105a27d363f4f71273a20d0010fd`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a05837526fe00223759e8d4a997d16345eadd06e863fa822ff79f7b5243343`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cf8a57886874429df642e8168365c3ecb7a063d42bb23e7f1f2c1e19dc68cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93173c29b543a157fcdd4fbac48cdaf4aca24e2c09177e19d20f7987b6e468c`

```dockerfile
```

-	Layers:
	-	`sha256:bfa78d355a05f618bcb520a2ee2043fa052ec431140c725530bf4ad0b42484c1`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.0 MB (1044135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336848c7176ed259cdb0ee73a90625f3667393472804f7ec51bc8d9841dbda2`  
		Last Modified: Fri, 06 Sep 2024 23:18:44 GMT  
		Size: 19.7 KB (19747 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:87d53f18cb03faf39025e6db99bf4ad236975ecb76be2529ce4334e0325d1dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11954923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47be54698bb5bd87023a358dec43509e3aaa872bb547aa782995b165d6923c3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e60bfcee050c6b70aad1aff59b0cc5cc8f1ab23c474abfe881c2e91992bdf49`  
		Last Modified: Sat, 07 Sep 2024 02:26:49 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8921b0dd188b3df9cd088ece4c0ac1af24b81b41396833827c2f60cef25457`  
		Last Modified: Sat, 07 Sep 2024 02:26:49 GMT  
		Size: 11.0 KB (10961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3801edcffe4b3c8e620c125dfe0804425e5b1342308e5d0c4e6dc322d6ac4b63`  
		Last Modified: Sat, 07 Sep 2024 02:26:49 GMT  
		Size: 2.9 MB (2904676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601ef8428cd417a44620b8b2429bd9ff1223b7a2f34cb82eb1a6cfd65784fbc4`  
		Last Modified: Sat, 07 Sep 2024 02:26:50 GMT  
		Size: 5.9 MB (5859082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a073d5de0962e4757190ef47514120247ca6d4ad755db2bf985b3df6893c2626`  
		Last Modified: Sat, 07 Sep 2024 02:26:50 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e6554369bdb6d914ebbab9109297c13e950b2bd466cfacfddd0985b2e94537`  
		Last Modified: Sat, 07 Sep 2024 02:26:50 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:26a9f3f6fb42e6eb85f54f4bac52114aa8e485dc8f1b56966aa8a59e57e59e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4869b18b5fbcfd2e5bbae29ca44d9b6691b18ef27d0347e6e0a7a4da5726db19`

```dockerfile
```

-	Layers:
	-	`sha256:1086a1416bdb94f398d34b7ec9b654632b08e64bb197f7cc320845d229c23c5f`  
		Last Modified: Sat, 07 Sep 2024 02:26:49 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
