## `clojure:tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:a10a85c6f878e9706e52f5828734573d2761eca77668d7224bdd289c646ab23e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8d1ecbbe89e0043ea0637c26cd1a832de23e05f17921b1890965a2468e88248a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246897170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463f80560e80783a9de9340e8c74167d5f23b39f75b9ec40a95f911f1ee583c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23745a0a3fa2eecc82235cfbfdc047eb75080a1936768695246ff1e696446319`  
		Last Modified: Wed, 02 Jul 2025 06:45:18 GMT  
		Size: 157.6 MB (157634472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b13c043521ab77780725bab49ca455dbba11d32fd875022db5c3244b2ccf5c`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 59.0 MB (59005612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87edf4bb058285014bca408e68496206c8e8b13ed75ab001bb1857dfd31f49be`  
		Last Modified: Wed, 02 Jul 2025 04:17:20 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f9fbc3044ae7fd013b091059f436418988fbf53caa44afda195854b2c04d91`  
		Last Modified: Wed, 02 Jul 2025 04:17:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9cee1e0a5fd0e832448d18e8f12981c472b2c96d4d212615b764cf89edd0cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fe2c772d1b4adafa9ef2f8a9157f2c78c4ab60eb2c9fb359f121bd8dffdf9d`

```dockerfile
```

-	Layers:
	-	`sha256:ab5eeb3bf4cf7529bee90b144ce644206d5791b8a4b5a4daa260bbb148d43c13`  
		Last Modified: Wed, 02 Jul 2025 06:39:25 GMT  
		Size: 5.3 MB (5311836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c3e48b28932667447b45e39ca8231ebb34fa8f743f38f61689e767e58af2ad`  
		Last Modified: Wed, 02 Jul 2025 06:39:25 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a347470416642b0410c39cf3e6018ddfe4d0b15c9399f5e9851df0d3b1af537b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243811636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346c152081654f3a458ea9c71b42e025eace175aadc2ecc01e4a6f16814feb23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a08fc5d26ea0f3159fdcfdad3eef2cc170548dacf9c31f67e17d009f4de991`  
		Last Modified: Wed, 02 Jul 2025 11:47:30 GMT  
		Size: 155.9 MB (155928829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51687ff80a646ef7bdb89e9bf75b8c06c43d72db873d3d176172e9feee64ce6a`  
		Last Modified: Wed, 02 Jul 2025 15:55:07 GMT  
		Size: 59.1 MB (59137628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3310c489f61000111cc431b40941cbc792a4e100e2bb4d617d4297a756a49e60`  
		Last Modified: Wed, 02 Jul 2025 12:52:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f1a057c81b3d3460ea557ba57b7863dab4fce98d42de239aa8f257a8138e45`  
		Last Modified: Wed, 02 Jul 2025 12:52:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94ac5837e19f608c96308bb7d4e24e4f48e54b2f1fdbb096eee2557eef976840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee060e7c5d2c6fbfea18b383f70f64896b1418637be6b1a24874d32b39492b1`

```dockerfile
```

-	Layers:
	-	`sha256:e1c02a0f68b1545e60750c2b6a39ae475cd85d57729d662b330206ca4f8df820`  
		Last Modified: Wed, 02 Jul 2025 15:39:49 GMT  
		Size: 5.3 MB (5317592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8111b25a7b1f78edd269fa59a452a86f142963d3263f3e40fa610756e4eee1c8`  
		Last Modified: Wed, 02 Jul 2025 15:39:49 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
