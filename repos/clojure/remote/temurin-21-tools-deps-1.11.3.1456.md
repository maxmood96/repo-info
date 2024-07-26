## `clojure:temurin-21-tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:62a0814d166fe06003512cf0f7f70e9870cb95304767de197f8877596c59c6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:65bb16068a5e18926344c57a6b066edf237c5ee6ce4e317850f2f879695f7530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288648402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc1ae24af777d969e314d45f0a9235247d0785f4be21dbcd5083797970d97b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4300b0c064bbd3979bd0192d82aed7173fca8c3ba024244c8ae2dc4583e339fc`  
		Last Modified: Thu, 25 Jul 2024 19:05:38 GMT  
		Size: 158.6 MB (158579315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4130da8f16926bc174a089a745b070f9ff7d2c61093eedb36040642d13a52dd`  
		Last Modified: Thu, 25 Jul 2024 19:05:37 GMT  
		Size: 80.5 MB (80513971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e404b1e24f0a0d06b6ffc0fe88e6ad53eba3967d9f06987c2356a7e2b87f559c`  
		Last Modified: Thu, 25 Jul 2024 19:05:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85345993cec52850a5273d480ebbd7e76ced73c7f39fe9b171bff0cffa138958`  
		Last Modified: Thu, 25 Jul 2024 19:05:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:75ec7f3778bd9f2d431da2d45d97986bd83a5d2221ea14d91090900b8053d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29390095c2086e3427be35afb906e156bb0016c95ac1d8566b0d647092b5b2b`

```dockerfile
```

-	Layers:
	-	`sha256:5b44baacc63de5564dad6778c9491fb7ba555f114535679c95ca2cb9b226e157`  
		Last Modified: Thu, 25 Jul 2024 19:05:35 GMT  
		Size: 7.0 MB (7002096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0647518e687238e92f84d6e908f66a75e4a0eb8cb4dcc5580f8cf89c124ee90a`  
		Last Modified: Thu, 25 Jul 2024 19:05:34 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77fce144975c8105757f8a0a42bf98f7ee9a27a12bb59bdc4bb28f0c45a3c58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286594395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2999d82ec9b0b2f8e18496400364af21c3d6d04cebf154d76a3f9f4c3e273ce4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
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
	-	`sha256:41fd1a8c33e61161aebab6290fde01e1a4816d32fde4b90657a392d58d58dde9`  
		Last Modified: Thu, 25 Jul 2024 21:22:14 GMT  
		Size: 80.3 MB (80258728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466e5415378271ae8dc70beddf6b2b27e65d1b43604e0be3121472379b13bbe3`  
		Last Modified: Thu, 25 Jul 2024 21:22:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea52cfba905adb6029c79c4ec07811fe2057b95c65f5480675b65bfae456a947`  
		Last Modified: Thu, 25 Jul 2024 21:22:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:63c1bae04738f4163ff9d4764be9cc9866fa25c09bf555d7b5a64164dc0a65c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a80598d10362c327ad160d5630a8d8a4ab21a50589fb4a47ce242eee926ba`

```dockerfile
```

-	Layers:
	-	`sha256:f9238eaf56aaf4c690a9fe86ee5955da1bff21fbabbcffa46544c44d777653b7`  
		Last Modified: Thu, 25 Jul 2024 21:22:13 GMT  
		Size: 7.0 MB (7008555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b87ec2f5a798789af58584f44848479b0aa2590fdf1863221a7c49364d6f7be`  
		Last Modified: Thu, 25 Jul 2024 21:22:12 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json
