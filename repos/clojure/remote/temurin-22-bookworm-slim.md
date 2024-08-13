## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:a1738e81af253507ccf5ed71748bba8f09fa5317910c1743bd353f6c98a5c258
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0a6d2e7df1d0b51f9394279b5a65a8c77d8f78639d1567196e368d64d9cf4380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254633270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3a95c51c35f47464cfb6b465570dc3933f28e8d07713ba93c24791a6c5e177`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2f882b57155c1b63fa3afbc704c982868f22322db94bca4638bb3f43822271`  
		Last Modified: Tue, 13 Aug 2024 01:11:33 GMT  
		Size: 156.5 MB (156481579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6372d9aa56bb83ddd9cd3f8d12a2bbb014ff8d5066bea24454393cc083dc40dc`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 69.0 MB (69024420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a00cf5db8d19d6086ae0d0c439541d12fe46d8edac2a873e9a36d742f68625d`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3833e8c599f124d2c655cbfd1e330911188bc3e018b53e405ad09aaf48929d`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:110c67308f8a0028e13a1f33a2e4eec5bf77923580f2b39533a1455e06dae5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d633218c8ae3139b6f9c19d1b9e7fa01ba6b687ca947fe408abe3e452fbfce`

```dockerfile
```

-	Layers:
	-	`sha256:15a9154896bbcaa82d6c56048e7230354ac25e39d1fbff877b59183b9a0e37c4`  
		Last Modified: Tue, 13 Aug 2024 01:11:31 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f85bd8c9d9a48cb7824a7f0e855a383b7304a0ef52918d2c041b54a6d02313c`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a70f6b57a8f9352706271872e6cb9d38dc4c9afeae1ad5b52e22dba31174715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252434812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b419aed3808b851776ee9f2977d581be5b04aced540f3447d5063f7bebd7e21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f2eca2f194e40017ac8fef9f5d14b15efaa72a7dca868db3e663fe43a543f`  
		Last Modified: Thu, 25 Jul 2024 21:28:13 GMT  
		Size: 154.5 MB (154503730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4171f1d623c07abc8de4ee6ba8942632c3b8c41f393efe6e3bdbc1b7d0dc06a1`  
		Last Modified: Wed, 07 Aug 2024 20:17:51 GMT  
		Size: 68.8 MB (68773467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ab5e69ca2a8cd1b7d0e5ec999ee66b764c970d1e1580a5fae4525ddc27b9e8`  
		Last Modified: Wed, 07 Aug 2024 20:17:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90621a8d0699073ff58f74f189449749d8bfa1b367a4d6673e115fd56475be76`  
		Last Modified: Wed, 07 Aug 2024 20:17:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fecb2d19e3eae83284a39cbaec9f6f0a544a90585e11e43c759d38646ead03fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c121d46ebe49afd763ba6a69105f7124f30e322995ebb5d1c39d1bc72c9f350`

```dockerfile
```

-	Layers:
	-	`sha256:906083f1c1365045f7ce7cf0df7a059add3ac29e8a8c6929409e3f757b8fdd87`  
		Last Modified: Wed, 07 Aug 2024 20:17:49 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7f0941f378579f1b2e708ac38a4371d1c57b44518077cba33f693a88c1cf0c`  
		Last Modified: Wed, 07 Aug 2024 20:17:49 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
