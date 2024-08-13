## `clojure:temurin-21-tools-deps-1.11.4.1474`

```console
$ docker pull clojure@sha256:46d963e628b58a37bf6c3c93d29b34f4170745b12526ea36d9bc83129df4e6ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.4.1474` - linux; amd64

```console
$ docker pull clojure@sha256:b59d2946c22a98bcb8dcf3261df82fdd3e8e4746ccf164b710e58f884e87ceaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288588607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4248ef867490715846c9392b36ac885943be9090d1331551f6ca027444b935b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
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
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf328e13a4cb3b3f034e243ac84e123297cc05b5ca9ab674104a0432db7a5062`  
		Last Modified: Tue, 13 Aug 2024 01:11:29 GMT  
		Size: 158.6 MB (158579300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba750a8233361853dfba6ecafb53244d04e5b83a0ce904c1965c3d97d3b95d4`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 80.5 MB (80454188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687f481a174f50fda0b4c5933770d8fab77c4c4bb1d4af4558a98c33e057bfb6`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4b72f849b94d316a5a6ad878f5e2241a7c80377ffb219b6749b9f262b11dd`  
		Last Modified: Tue, 13 Aug 2024 01:11:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.4.1474` - unknown; unknown

```console
$ docker pull clojure@sha256:18c37f0864c312013c72a557139de7613581b9c89d8e04a1a9f6a90764e67eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162db3f992aee3acf01e5f390f60f70bb503081400e5cabb4f8cbda15cb56b21`

```dockerfile
```

-	Layers:
	-	`sha256:e9a87bcee9988b370d0d3aec907331349d96102f708677728d986e796e9cca64`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 7.0 MB (7002096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6350812b4f8b2bb05dda895a34814dfb01c3bd69ae7f19ad9dad492663cbe417`  
		Last Modified: Tue, 13 Aug 2024 01:11:29 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.4.1474` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a65c6365ed2d8a1e970337302386887d197777d459526996c702ccd82828b59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286534276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403b72be819b141adfe85fbd7e19c7ab7ae5f69f10c79746650437b0aff75db4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cfe8e625b59cbbdce764f2360958da104710a92c5313b85ee3c12b7c861ef8`  
		Last Modified: Thu, 25 Jul 2024 19:06:56 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482117eecd964c78a37e45ee289cfa3c9aa0526f9e4ce33f255ab502586a7dc0`  
		Last Modified: Wed, 07 Aug 2024 20:12:03 GMT  
		Size: 80.2 MB (80198609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6b35fe413a6c8e0a79e3c5f6d86ee670e3f313b8dc78f98b9aa2c3a9bff987`  
		Last Modified: Wed, 07 Aug 2024 20:12:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4d5ed51cb5e0a93961a7be98e358e99cb619991a83ae835f1127e2076e39ca`  
		Last Modified: Wed, 07 Aug 2024 20:12:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.4.1474` - unknown; unknown

```console
$ docker pull clojure@sha256:13f0f6e053b3822b09ea62e9296801d783e105c1c3bca8087970e44741f8f510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa85a639aef8b26acffad4d1a6b816e4da7bf8cd2c2177bb3265f2d8dcfc2928`

```dockerfile
```

-	Layers:
	-	`sha256:b86eebb8c06101bdf75ef408a437f65cf77fe9a639941aa970df49a8bb7c7d84`  
		Last Modified: Wed, 07 Aug 2024 20:12:01 GMT  
		Size: 7.0 MB (7008555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8e9bccc9e1dcc0c8313d6d4576badab2eb8989adf54aec261bcf012d162ce4`  
		Last Modified: Wed, 07 Aug 2024 20:12:01 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json
