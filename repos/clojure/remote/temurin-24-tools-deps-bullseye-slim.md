## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:6f7fbdc718584be7968304018dfe2d89045b055a71caecc21458d06afd0db4f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61c010eb2c9b2ad7c91023ae0ca7b6e1e570a187ee69bef6e8c6684984b4c835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b3708fb6664412b62b43589119b28827259bbe370fdd38b0091e8607e08c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ade5661204e6e829a6794399fe4630b1684e2a39ad112a2ad314b87b267e6e2`  
		Last Modified: Tue, 10 Jun 2025 23:53:30 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a70e0ee4ec10249b7a098ba46e4d2620ecbe082379b9a6430002ee6755bad`  
		Last Modified: Tue, 10 Jun 2025 23:53:25 GMT  
		Size: 59.0 MB (59005572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6b58653c1ae356bc714e2ff5e05444df1beeeade6799c94fd3487065b4f120`  
		Last Modified: Tue, 10 Jun 2025 23:53:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7a58fe448d023f73a9731fa54a930b43ccca1000f01a6373341ce04123b32c`  
		Last Modified: Tue, 10 Jun 2025 23:53:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af8a8c9c1dec625e48bba13acf9567986dda91413cce88403080a9548dd76cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee16c7a4849013fafaa6594c3b73886430bfdf7e9e593cd5186f85c5d0f3092`

```dockerfile
```

-	Layers:
	-	`sha256:9094269d32f82f65b0873e4a34f69e205322237d54264d229cfd77408f2cb87d`  
		Last Modified: Wed, 11 Jun 2025 03:39:49 GMT  
		Size: 5.3 MB (5258684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a0d364bb1f5a4af3d75bbdefb520eb2de90af55ff9261073f6d2f848d5e6d1`  
		Last Modified: Wed, 11 Jun 2025 03:39:50 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31d7e315e79d97f37cdcbbdc6e1320707184a78d989e1ee33a3aa74b65194731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176973917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d007a5e088582cfe55a218364dc457ceb81465e865893ef77b7f8711082dd2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578690a96e2e4ba5fbf59b73b69955c75b8c7c6c842e0231034a946fbb7c86d0`  
		Last Modified: Wed, 11 Jun 2025 08:45:53 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff363b88eb63e6f24274f12213c798a29b4e5199d4e449e8babc6f6bc28b798e`  
		Last Modified: Wed, 11 Jun 2025 08:48:51 GMT  
		Size: 59.1 MB (59137417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240c55fd9ca18700ab0a62226b0a15cfcc59fe3c3b9681da0551b9fca492db98`  
		Last Modified: Wed, 11 Jun 2025 08:48:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d981fc5f187e13d86339879ca23c74a21be83659b6a68f729aaacf5ff068531c`  
		Last Modified: Wed, 11 Jun 2025 08:48:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:afb64f43d94bdd1f7f50bf630deb1a8f6b046cbe23f2869c0e2058ffa45a7728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aac6a1fef6befb7e0bffdc19abbff922d1003b325bef727c2ce14836a9b5bc5`

```dockerfile
```

-	Layers:
	-	`sha256:170f588293d383c92bae1c3480970b9cfe330062d1c480129cde043b2d2e1221`  
		Last Modified: Wed, 11 Jun 2025 09:41:01 GMT  
		Size: 5.3 MB (5264413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7192938d0892a1c72923184f9d7ec2faa0726c6b617327c97611cb962d0e1ae0`  
		Last Modified: Wed, 11 Jun 2025 09:41:02 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
