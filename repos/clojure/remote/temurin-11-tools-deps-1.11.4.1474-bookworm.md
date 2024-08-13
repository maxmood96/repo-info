## `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:48a45fc10ea7a8440ac2126f2c658ac5804cf7b01eaebbef95555261041b7110
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a114d815649406e7fcc3ae52e2adcc3731b07215e8a9a335f130e94e06d5f073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275558696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57f372142542bce2346f3085ee0d6bb76fbbd9769462e0a2d4dc8d1b91c16c4`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2fcd7e9b200c9d9cbcc4b48356f1f8625a2f80907be76c66763bc8d75508e`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 145.6 MB (145550325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8785ac027c1ad1ef0da25393ff1aaf52fb39a4a7176a60b63107d18a0af44a`  
		Last Modified: Tue, 13 Aug 2024 01:11:24 GMT  
		Size: 80.5 MB (80453646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2605fe4a962745d23b1310c63572026714b43c8ccd0d7a24e6d1c8c3f77a014`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1229398c65a9bc5c14903c05a0d9ad719fdb1eef76eb8d6a09b0296ee080cc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da8425ef66b1bac5e5366de4136042845c600aedf6cd3079a091d7829f2f64f`

```dockerfile
```

-	Layers:
	-	`sha256:172899eb71b60fbb2144c2c31fd4185c49cf02e3077bce43792e7831cab6d1cb`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98576de13ddf5d63cdcfefe0b7b5897a68f2ffc6914a8a6ae8807d4d41dfdb8d`  
		Last Modified: Tue, 13 Aug 2024 01:11:22 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f065b5bd85c06d1ceabed90f701ef1632be6ed71702a54b47d98c652824e87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272143533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2102787fc39138668687b84bc90751e65a0fc869a602d0d14dda1aca0ec418`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f67d9b073e52f0f34ce969f83aeca603f4549e813031ed7aab473b907f4134`  
		Last Modified: Wed, 24 Jul 2024 11:23:55 GMT  
		Size: 142.4 MB (142356360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0985a5e869b7a308f20702df1d6c6dc13983a2c3a12fb7a32f6b5af773309c49`  
		Last Modified: Wed, 07 Aug 2024 20:02:14 GMT  
		Size: 80.2 MB (80198084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df80d79090685148ae8673e254468b9581f90f588551b78f6e221d101b45c0f`  
		Last Modified: Wed, 07 Aug 2024 20:02:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:371c3f804d93cac2df97ed28e84a9ce01890ae739add238ec268312ddc0c97f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af16653bebff335ea19c1235f15b57e1303cb51d6d2f13be28c2ac3ad4f5c30`

```dockerfile
```

-	Layers:
	-	`sha256:3d426b09dea96a15479164ec5e3c1c6e520fd340b26d5d9a537c6f819d6aa5ae`  
		Last Modified: Wed, 07 Aug 2024 20:02:12 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0349a148d0c92dbf2e2c24345125181d0f2c258a3f6c19ef81a04d9d59fc9bad`  
		Last Modified: Wed, 07 Aug 2024 20:02:11 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
