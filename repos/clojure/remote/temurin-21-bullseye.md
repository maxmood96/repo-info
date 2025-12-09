## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:e70149c53d351f3a9876420a1d12189039a54d7767ccf7045cfaefb633649e65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:aa300a8eb2f5669bf6acd016f6666942abaa0e20d98a66130eb931561e553f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281144708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549e110386196cb1bd06fb213878c9a40a931dd4dab00fcb201a20847fb2d5a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:55:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:55:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:55:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:55:09 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:55:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:55:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:24 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b95e22a66f7bacfd46b6f519345a1502eb3ad6fa96b619ee459f14239ae27`  
		Last Modified: Mon, 08 Dec 2025 23:55:49 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28452fc8b788ba1564245c58666ab503447d93b523ba01540c27e7b2e3e53acc`  
		Last Modified: Mon, 08 Dec 2025 23:56:01 GMT  
		Size: 69.6 MB (69561215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693fa14ed2823cbfeb04220cef42ef00fcd9b9a65bd7050c15116e63c5d55b9d`  
		Last Modified: Mon, 08 Dec 2025 23:55:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cfb57bf46315edb468cc5b456bef33f9fa6b8fe8692886f24a57edaa9d9b1b`  
		Last Modified: Mon, 08 Dec 2025 23:55:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9425de7073eb1716c6acee0466e71986a18dddd0e82b8e0cb00874575cffc6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf48715d42eaec49b688a1db68fc89e934edb8078030c464d0c152fe04be30f1`

```dockerfile
```

-	Layers:
	-	`sha256:58cded76315fe450a55e939de65c0a25c58b9532cfa6a0e77c1b1d2d1900c9a1`  
		Last Modified: Tue, 09 Dec 2025 04:42:33 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b072c041f40e3ef016955d4e159ceb096e2084a2c8a4d13afa9ff3461e60c592`  
		Last Modified: Tue, 09 Dec 2025 04:42:34 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14aa34cb32d240d1755841ab471529c99f5e160e63de8e36043fd6f9a45e202b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278054529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f87b0346c525fac157c8ec82dedd74e55423442d888c231e2facf597ce014f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:02:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:02:26 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:02:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:02:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2778c31fabeb678c1f6eba9f8b36a8665809f91b30d55fa89165a3ca97979b79`  
		Last Modified: Tue, 09 Dec 2025 00:03:19 GMT  
		Size: 156.1 MB (156107637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c592b0ec4ee00f2c2ab0ae826e9265c04a4c3622854d3c90b28f657c39883`  
		Last Modified: Tue, 09 Dec 2025 00:03:17 GMT  
		Size: 69.7 MB (69688143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250ff1cf4a4770d34e23c5314a9b4051fb54e108f2539aae05bbacb8e2cca4f`  
		Last Modified: Tue, 09 Dec 2025 00:03:10 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4da2735cf1ecc54f3cab62b0970e20646fd8433de667fb3e92cc1f69b3fa0d`  
		Last Modified: Tue, 09 Dec 2025 00:03:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d0da1a7655ebb69bd1e64995d1e62b86de3cdda095a2b430913319451548279d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6028c2447157124ce5105aeb20e08240b02b0d66afad449324dd9fbd4568312`

```dockerfile
```

-	Layers:
	-	`sha256:1c9a6004bd9e3fb15c7dee06dd488e135fb4c6a3c38084982b22c79401c5d27f`  
		Last Modified: Tue, 09 Dec 2025 04:42:40 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41306c050b936c09dd1abe85bd1b7b5ed02b97ce1065949e8fbf808cdbfe1c1`  
		Last Modified: Tue, 09 Dec 2025 04:42:40 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
