## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:d098544012c60127a75ac80983a0501a3eb938a890d8f57f87b89f2672214a8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:045de1de4d622f154016dde04879b26beacdc9193e4f9aadb7e1b25dd93931fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269581820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a500aa2e72af8c283d389903e643bfba4e7411381f0e8dcb13f8d418fc5821e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fccaecda49404fe1f7c5aaea9adc036f2fa1c847eac58069af648c0c9a49f6`  
		Last Modified: Thu, 17 Oct 2024 01:13:48 GMT  
		Size: 145.2 MB (145166496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd9a7c00f5727ba728a3fe6d61ed784ef071cc5a37ac6407bcac6525cefe4ed`  
		Last Modified: Thu, 17 Oct 2024 01:13:47 GMT  
		Size: 69.3 MB (69333674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d427a5f4ad8afee0e3fb1c0a0c1391d817845c709723eb763509db8256b419`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4f040036e2728917f3d70ba920f4e6d7c3bd63e98ca045de03968acb9996f0`  
		Last Modified: Thu, 17 Oct 2024 01:13:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e1aa09f192c4bdbd01b358c382d17a2efa0fb7654ab1c08ef0d2846d9cf4d91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04db7632a8583f7d636c7af97a189023c31d438c94ffe65c5809187c00a56eb8`

```dockerfile
```

-	Layers:
	-	`sha256:fb34f252c4c0a11d58fc0677406b8cc3bff1a3e3e77451b64367fa0a94e9eb0f`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 7.2 MB (7189453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffd2c3970001f4bf83add3d58b7e397e2f8aff2049d74d7bcb28940c3b95f95`  
		Last Modified: Thu, 17 Oct 2024 01:13:44 GMT  
		Size: 15.5 KB (15478 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb903857ec5338ed943dc1210907780ef0c6ee7113dd5c7346cfaab441c7a963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.2 MB (267161593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89788ae1d2efc997f2aa5615769bcdfd13c230fe812548887f63d8a80b37b72`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7bffc00dde25142de9c36d297b5f3ec79b326da54b5ebba4f0b05db8be8992`  
		Last Modified: Wed, 16 Oct 2024 02:23:02 GMT  
		Size: 144.0 MB (143959504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d375a3bedac10629f44e68e76c56102179bebca2f778d4f89cd58c8144183280`  
		Last Modified: Wed, 16 Oct 2024 02:29:14 GMT  
		Size: 69.5 MB (69467180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad555b584644bef5118375e85c4c334ff019f667f3b92dfeb7c9dd6d9904a757`  
		Last Modified: Wed, 16 Oct 2024 02:29:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac2c862a0128bc691c03ee4cc01596c2db49385186dfa4b061e46e3bd56e71`  
		Last Modified: Wed, 16 Oct 2024 02:29:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:54f77492b0544a97d28f0cabd46ff7ed5999beb7c25009d51c08754529e95cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d800660760e620bc81f08483c3ba87ac10328f5db62e814afbcabac2f70a109e`

```dockerfile
```

-	Layers:
	-	`sha256:c85132304d8592db0ff57a60556807e53d4a051d5aeb5a0b3c3696994bf6247a`  
		Last Modified: Wed, 16 Oct 2024 02:29:12 GMT  
		Size: 7.2 MB (7194466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d6b955f861e3ee447ff0e2484e9014b62edae85b39dd3cde59c5d35386f899`  
		Last Modified: Wed, 16 Oct 2024 02:29:11 GMT  
		Size: 15.6 KB (15582 bytes)  
		MIME: application/vnd.in-toto+json
