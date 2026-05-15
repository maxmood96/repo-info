## `clojure:temurin-26-tools-deps-1.12.5.1638-trixie`

```console
$ docker pull clojure@sha256:149e6021c1682ed9b194c0eaca3c56be174aca9aef463e2de36511568d599183
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

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:db495c5b68fb5c241958a37264de9f6fca480a8639ba037d1c869211e0e86b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229363089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145876a37faf25d53ec397c4510d63d1d0c5a9a295043d17baedcd1f1e77c0bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:37:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:12 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:12 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a09a381e8e3544b34f6e87381a8f63be9426dccb0d09e12ef74e2edeb9743c`  
		Last Modified: Thu, 14 May 2026 23:37:49 GMT  
		Size: 94.5 MB (94455698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd37cbd9507cf0f46df91818b89a8a3060419a53243a21bb6e56ed2d81c24c8`  
		Last Modified: Thu, 14 May 2026 23:37:49 GMT  
		Size: 85.6 MB (85604027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597d7ae4d233718effe8f832e827693ade7c355125956b83550fe9184c59abae`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9811f79f9658237f733a346662cddbcbc25f20c80ed0a95a55428c0ef54e0`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ac8a74989c6299632991f0ab2b9a804b8c3a45f42b414a3ce35eaaf23402b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeb5ce93c03c9aa96af066e891862cfa56132d08f252714f852554cf5beb2f3`

```dockerfile
```

-	Layers:
	-	`sha256:81d15df0413748af545502e03e5b92b48d4b5eca90e4e6992038c4dd0cebe63f`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 7.4 MB (7436259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b3ac40c562defc8d693e216fe3706a1e2e56f2cf04275a8f986bc370e72aaf`  
		Last Modified: Thu, 14 May 2026 23:37:46 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:919f82216b107982b3d359c4577969a234333fe8d79cdfc20905861ef41c653e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228480740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5429d4fc81ac39586e231e3fad5ea294e1d739ace97c0efb626ff348b83787d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:37:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:21 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:21 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7a796e73c43f88dc3a4cfbf64d85de02d42f746beb81904799a4bb8221befa`  
		Last Modified: Thu, 14 May 2026 23:38:02 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515c2b70c3d49f63ba53c4180e55d575f13dff6232831959995d3f9b10841c7`  
		Last Modified: Thu, 14 May 2026 23:38:02 GMT  
		Size: 85.4 MB (85415082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2df1f46873ea95739190cc6e2de98c7e0ae856025a1e945561f80d749037acc`  
		Last Modified: Thu, 14 May 2026 23:37:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c706b3294a948869ca8eee2a2cadcee9d5d1d8b59cad0c1540517073f8dc89`  
		Last Modified: Thu, 14 May 2026 23:37:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:618fc80e9cbfeeac5cb77fbbd82cf49d50b9c128f29b01039f7ac0b2ee43a628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3dbd81d704d41faaa387cdcffaa91a95e6e27d8aa3afc5fed5c278fb400a23`

```dockerfile
```

-	Layers:
	-	`sha256:5949d6a59ae62b9884931c49b60d54d79a30865cdb148bb5ab81989523df140d`  
		Last Modified: Thu, 14 May 2026 23:37:59 GMT  
		Size: 7.4 MB (7443286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb352f9de5bc4920870b75bc6b1b51fe75619155c91dcb5252472ab6a3e7186b`  
		Last Modified: Thu, 14 May 2026 23:37:58 GMT  
		Size: 15.9 KB (15865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:725b3c87cdb677eb764b0b3d03ebd342b006448c4d8dea0a85781bed377715a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237914133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58a893558892dc71cacc377c1677ca9577f3b74d50be3564e19d4614c756b1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:48:10 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:48:10 GMT
WORKDIR /tmp
# Fri, 15 May 2026 00:00:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 00:00:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 00:00:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 00:00:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 00:00:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380ed992dc2e5079fc5af8b7e42121e0c356119cf7446f3b8707b481cc61b56`  
		Last Modified: Sat, 09 May 2026 02:49:19 GMT  
		Size: 93.8 MB (93781452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0e19b226cbf6ad8ff76c253a54a5db89e299693cdfb964535137f1f112dda`  
		Last Modified: Fri, 15 May 2026 00:01:03 GMT  
		Size: 91.0 MB (91008471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc2a525e5066aff69357786754a418b995ae6ae4366618940e177deadfe34e4`  
		Last Modified: Fri, 15 May 2026 00:01:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f37d7948fc9d583ee594582809e09aaf99a9d323e3ea43d3337cb8d7f1361b4`  
		Last Modified: Fri, 15 May 2026 00:01:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6c85deb444af00ed74ecac860ba36e446c80a22a25d5c5b1a14e20e6ad2a116d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb59bc98241b940295f957e86a692a1bed37312550a58e6c9efead8d8d996402`

```dockerfile
```

-	Layers:
	-	`sha256:e4f0e34883c9d8b10c14697292e115248b31d139767e5f88b14e7752b7d2c358`  
		Last Modified: Fri, 15 May 2026 00:01:01 GMT  
		Size: 7.4 MB (7424616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c93aef2785e58866618346cfe159013448c560c9092c6c45f97ccd759c5ca3e`  
		Last Modified: Fri, 15 May 2026 00:00:59 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:93ee5915edfdc255450660e75627c4289730004a6320d1814a0712a6f293ba30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226486522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10176c99dd8a237d97f64c526199c1a49adc688a62a69a49ab3f9c9acfca20b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:39:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:39:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:39:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:39:17 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:39:17 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:39:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:39:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:39:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:39:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:39:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68251c48c33aafa4dc044130cfcee6a4e957ac5f5c475d6d3200fc99aecf6677`  
		Last Modified: Thu, 14 May 2026 23:40:01 GMT  
		Size: 90.5 MB (90547720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acea7655c4f58ea2003303074bed99a2eb11e4476d8159b488bc45057aaf004`  
		Last Modified: Thu, 14 May 2026 23:40:01 GMT  
		Size: 86.6 MB (86565454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6ef465a2138a19ca217da6c06beeba9d97bdbc281bab7dfde3ba33d7e60dfc`  
		Last Modified: Thu, 14 May 2026 23:39:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d35cc99a095ad8940009c6aac010247a7b05c29a33d987ae0a6de5d9cb2126`  
		Last Modified: Thu, 14 May 2026 23:39:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:609540ddef67ff5f28258068c8e5fa1d7e030dc77841a997b4e75f9c5942585b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db56c524e455886de883fc098772ef9e368ff0fceb6e85a004f740dc202b2f34`

```dockerfile
```

-	Layers:
	-	`sha256:017b8e4c9adb22399e1d487a223f70de13082c6903a9a0819dda4e89d2d13133`  
		Last Modified: Thu, 14 May 2026 23:39:59 GMT  
		Size: 7.4 MB (7417367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03d844634a553cf998a906790ebcf36104c6035080788d7dbfe53b7b1d7063ec`  
		Last Modified: Thu, 14 May 2026 23:39:59 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
