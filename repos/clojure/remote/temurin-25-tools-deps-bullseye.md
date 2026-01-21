## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b417b25669f1068630e24cd018698918c87b450b645b3431c220d1c9718b48de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d1e0350725f0d433161be22c36dec5e78b484a56a73d960d9b1a15a59cc6e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215359615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d241df22e267367e1eac5635936039cd5b726e71bb51830347be24e5bf2952d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:06:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:06:09 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:06:09 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:06:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:06:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:06:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:06:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:06:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e59d09db65a554b22becbfda147e478975b2974cebd1fde08dcf3cfdc6c79`  
		Last Modified: Fri, 16 Jan 2026 02:06:45 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d5dbf4fc1bb0b43d6e7dc3c1260bf8cd36c86a640266bf03f980c98c2b5fc9`  
		Last Modified: Fri, 16 Jan 2026 02:06:44 GMT  
		Size: 69.6 MB (69556807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391181d4814b5b4493771282112ffa461d0deeb55db584190d5d973693d9ec4`  
		Last Modified: Fri, 16 Jan 2026 02:06:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfac2571d513f3e4007d260384279557272b7eacc3c181af51cfdf802637aa91`  
		Last Modified: Fri, 16 Jan 2026 02:06:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:379ce3f4780239246335c9a2cc887647c1885248d80b931038fa13ed1ff49ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c665cbd1cc2e48ff93e64f4166cd8392bc0609ec9ff1ec39d6ca14b2ac0f9a`

```dockerfile
```

-	Layers:
	-	`sha256:cf081f733709f5e031d360013fade1b7c9ade6f285c600c8099d6beb7fabdfe6`  
		Last Modified: Fri, 16 Jan 2026 04:49:38 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df65d6de5debafbbc385e55bc0f037d12ebf682d19e825a05c721edd2ee6e06e`  
		Last Modified: Fri, 16 Jan 2026 04:49:39 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0134de303278f91079722abb57163b8665b0663f6eab4d2aa14351eb3831cfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212998229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed4aad2a1c2643d86bb4bf044c605a61852afeea3002bf5f6db51857def38a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:11:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:11:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:11:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:11:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:11:26 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:11:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:11:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:11:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:11:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:11:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dde804be7ebe3d96d31b95294bdd0cd2b25074424fd96a0f387cefdc0886331`  
		Last Modified: Fri, 16 Jan 2026 02:12:03 GMT  
		Size: 91.1 MB (91052500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a269da420e9a491602c804189b43d8764b0b2be3897005148189c7f80f211c1`  
		Last Modified: Fri, 16 Jan 2026 02:12:16 GMT  
		Size: 69.7 MB (69686919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9e096974554bb6f6f76c822b7dea44d3f26cc4e8fbfc5ed9da4434fe7059bb`  
		Last Modified: Fri, 16 Jan 2026 02:12:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b773d01ca83afc496b2188097d5752524592ab8aac98957fe445976b7191a3d8`  
		Last Modified: Fri, 16 Jan 2026 02:12:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:37b72eb6575d8798007cafe2ed9548ee53497a8cccaf00817914bfc74737c30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cd6c8eb7af518573b4b95f9e2516ce8d078928eb5a831c7f92d4f6e04f8984`

```dockerfile
```

-	Layers:
	-	`sha256:f4581f051df662eac2e6739a9e0b39f336c0d16a67e55e2271d116351605f321`  
		Last Modified: Fri, 16 Jan 2026 02:12:00 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08d3ea1563a987fdd3a7877bd1f64ab0f07c05d8fc51ecce75a943c9fe39bff`  
		Last Modified: Fri, 16 Jan 2026 02:12:00 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
