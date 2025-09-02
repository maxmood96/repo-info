## `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:af931b34460ec3cfc5e2075081c700995afe116f03a80e666a04e95be5aa541e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:734bfc126610901bd8db2bee50fdde1366438df295b987d2cd59c54721b963c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219609114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd637ababdaf8b27cfb295b9a18e6a3844f8f72611813cc9fea46f31a7e813db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84cfb2d7ccfac103f59281f53c89d0749beae685471919b4fd9b1ed14c1653b`  
		Last Modified: Tue, 02 Sep 2025 01:56:51 GMT  
		Size: 90.0 MB (89975189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55886df47d5632e7e34bc999fcb3950f15ea6889136bbf4b9314aaa4bdcbe7c5`  
		Last Modified: Tue, 02 Sep 2025 01:56:57 GMT  
		Size: 81.1 MB (81138371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdb3b500c5c26c71ad1d15e54b209ae82541d046f14e86d5d9b33a4f194e3c5`  
		Last Modified: Tue, 02 Sep 2025 00:55:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ce20d5aee5a0cabbccd123a6faabccb238d17423256f7a6fe111bfe8254495`  
		Last Modified: Tue, 02 Sep 2025 00:55:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb1e9d1b72cd50764b962747d2d23b5997f4df03e88249c94647f6c23d4f1388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a84f630db5e2065c17ffc47a837f53edb5a2e53952613a7a2a6558dd330e17`

```dockerfile
```

-	Layers:
	-	`sha256:f1ff10375820f354137b2d15688db746ccbfdd3c308e54d155f4820ad5685ebe`  
		Last Modified: Tue, 02 Sep 2025 03:43:00 GMT  
		Size: 7.3 MB (7319629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df3994cb4c76356b5c15ed148e512f6298e8b7daca06a757c1b32d140384be34`  
		Last Modified: Tue, 02 Sep 2025 03:43:01 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4126312fe9c91d3ed32e122dc2c826da3708c70a5f0a14062324e3ff5bec4555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218445292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddec97bc33634c01d48ee6d117a05d8c6ebeb1237db1d118b2580191779b047`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1f56c74e08dc9d74a3bb040cd1383eb068ba2ab625b9dfd5a39a8971a72f76`  
		Last Modified: Tue, 02 Sep 2025 08:22:06 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6561cda3695128c3ddd17291999c2407a9ede34856c106066a96a42070cb9a47`  
		Last Modified: Tue, 02 Sep 2025 08:28:02 GMT  
		Size: 81.0 MB (81009301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a44185cca88f0891ece630c1679d9a8d51b7159711cc0e8fd4463f1fa151e2`  
		Last Modified: Tue, 02 Sep 2025 08:27:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4b2317f56d7250302829e2f88329052cb4ba725705d7f2834ef5cc63fce2bd`  
		Last Modified: Tue, 02 Sep 2025 08:27:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a34ad82cc33280d902d45786c09af57afd4df0db3f5a9454c64794367e23960d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689b02266e576c556d7cbba5f52dba96de44390ee19575f3e99d3e7a98955534`

```dockerfile
```

-	Layers:
	-	`sha256:28c6c9d8192cb5dbe2d070bacf9a5b9f7567121228e5b445253a40fdef9a845d`  
		Last Modified: Tue, 02 Sep 2025 09:42:27 GMT  
		Size: 7.3 MB (7325413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fce69053cc02c61117beecf3ac4d26119f4b512c9c193c18805924bd7dfeff3f`  
		Last Modified: Tue, 02 Sep 2025 09:42:28 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cff21f7ecc693791d9de3fc7531c0e34efa98b18bf99606400a8d0389f77be3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229229991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c005f0782dd12e08b42399944bd46756a6ae4feb3fbd41a2271cba53d619d603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf99ae33abe90ac926d583e1bb0999d30f5d908ae09b020378fb9feecd06514`  
		Last Modified: Tue, 02 Sep 2025 09:11:40 GMT  
		Size: 89.9 MB (89918160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0878dcd66ccf213a640a3b3bc2e4f17c77fdf7efdf7665c42140553b7759a0e`  
		Last Modified: Tue, 02 Sep 2025 09:22:20 GMT  
		Size: 87.0 MB (86972710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594a650855b7633a0839606343a7ec4d6ef493449e4fb9222ea447c2bce47c3f`  
		Last Modified: Tue, 02 Sep 2025 09:21:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347cd2beccd1455bfd5bd0d21948ecf202a77ed2d0aa26eafad2b6b446473fa3`  
		Last Modified: Tue, 02 Sep 2025 09:21:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:186a2bfa65432af78ef0d7254fec15c2105fdde03232959bf88546258cde51d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cf01a342a38dcb190ed56057324d7e78d1c244b1d2d9009a291cd5d38b0b6f`

```dockerfile
```

-	Layers:
	-	`sha256:089587dba854dadff4bc7d53902a2b7dada7e20072710c98f4fbe39d0c41d1e8`  
		Last Modified: Tue, 02 Sep 2025 12:36:44 GMT  
		Size: 7.3 MB (7326143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4531b9db1681bf6affbf61c51a6917d7febe867fd8947a842ade02274fc4944`  
		Last Modified: Tue, 02 Sep 2025 12:36:45 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c3751a067f1e7d7a355109a5fd8dc4846d80d1c673460959b4fa9359242dd8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212331043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ef6687daa4efcd99d5c4271d57da3383a0c3499b9c887a8247d909b12b9b6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b75f461e4b0c1938bea66e5b4d741de3bbf5a4e9ea18ed9da697c0fabb0f16`  
		Last Modified: Tue, 02 Sep 2025 02:21:21 GMT  
		Size: 85.2 MB (85226362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf49e969401808844b7286c4dd8209243a48cd96a33adb668956fdb8cde64a8`  
		Last Modified: Tue, 02 Sep 2025 02:26:09 GMT  
		Size: 80.0 MB (79953773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8640bc1a3547a8681c0b93d9930c26f22b764ef05207df3e68c0ade916fccda`  
		Last Modified: Tue, 02 Sep 2025 02:30:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42f47524ad1701840752861e35d3e5d528d4281899aad5854ffcdfe4bc8b7d3`  
		Last Modified: Tue, 02 Sep 2025 02:30:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:152ccf16c072f7ed418583eac82dfc6a1d4fa590511b046f3ab07a5cb8572a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32de831ac301d31dbc9e88fd273dd1bf7a04feba5bb5ffff6d3b097f148d2df`

```dockerfile
```

-	Layers:
	-	`sha256:f6488002db2c017f44af76e1c77dd7bfc06cad67bf5048797953754820bca326`  
		Last Modified: Tue, 02 Sep 2025 03:43:19 GMT  
		Size: 7.3 MB (7313496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6119cc50f537e691e862418470707df9916473f8448cecee528348b83d15945f`  
		Last Modified: Tue, 02 Sep 2025 03:43:20 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json
