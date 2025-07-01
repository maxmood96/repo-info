## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:f0db3165c3ab287115e7073f81399dadbcbbb33f7612baaf1cde665e224d64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:931351b5433137e20619c7e15d772cd8271f5b0dc2b293d09adb514c1c0e4840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213117526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518358889ffdb9cd06817be939866635bf0465ffb3edbb0f04e26d723879d312`
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334e521940e199784ca84de06ebfa80920166a99da4f768432322e1defeda522`  
		Last Modified: Tue, 01 Jul 2025 14:01:51 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9a03191608d89db5ef2e5d2d68070c396f8b5880db6fe5b91801b4ea3b373`  
		Last Modified: Tue, 01 Jul 2025 14:01:42 GMT  
		Size: 69.4 MB (69409659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb7a1e1b183dece045632031355c36ad47b4671833dea96d89292a880eceb45`  
		Last Modified: Tue, 01 Jul 2025 03:44:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ddd87206c9fa34b06a30efaa89c8cf4eed166bf073b0fe13339419b2169a8f`  
		Last Modified: Tue, 01 Jul 2025 03:44:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2437f6656bcfcfd1235bacddba98b697b8c91fc93cd02a46aff50c8d788204ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55db37c936edd81844db6f242a0ca2ef6b81479f3f119f7237de57420da65803`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7497b5ad8811b035420f956f6a83719a5a21d9df28a5c22862ca3aac2fa2d`  
		Last Modified: Tue, 01 Jul 2025 03:36:53 GMT  
		Size: 7.3 MB (7346284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2c261fda265459f8a52e8457c164a021ae72329a3ce646822b989a5ceea4a5`  
		Last Modified: Tue, 01 Jul 2025 03:36:54 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc12b6539ba661af20dc13765bb3f9d5dfc463411575e7d57973a9811eec65eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210882165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68daaef7148dbe435c7aaf1b5b9c21cea76141f0163abc53c45f8b1eb5109a65`
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
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6716ac935c9bde9dc6156b1d0aa05d5a475a3607d07ca12e73fd2fefd96e11e`  
		Last Modified: Tue, 01 Jul 2025 12:38:11 GMT  
		Size: 89.1 MB (89091290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f13c55b191ed690f1c46bc30a271a834a8c3fe5d27c9dd22a72b2d9ae1955a`  
		Last Modified: Tue, 01 Jul 2025 12:43:31 GMT  
		Size: 69.5 MB (69537581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2ac0bc0be7f47c201f7114f49ca03b2a0a9df99f851837ff7b3758296a9d0`  
		Last Modified: Tue, 01 Jul 2025 12:43:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c21e6f9216426241b5caa51ae38c45572f87bc0782ef1e96eac28e84ade8296`  
		Last Modified: Tue, 01 Jul 2025 12:43:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a47d42b55d1cf3b5401f25519bcf4bed5599b1d5b9634777ff3907f4b4da658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641a8adf4a96e35ccf6642d9190d42926e2cc758e33c65e3c54b9cf9f3c81dd9`

```dockerfile
```

-	Layers:
	-	`sha256:21af3aad3d0f8c6e6180b14821873642e32cc705eb49884acda6c28103a7923e`  
		Last Modified: Tue, 01 Jul 2025 15:39:58 GMT  
		Size: 7.4 MB (7351380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec52110b4396fa11355ff89f623a061db50cda63f533ff7441aaca1addb54588`  
		Last Modified: Tue, 01 Jul 2025 15:39:58 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
