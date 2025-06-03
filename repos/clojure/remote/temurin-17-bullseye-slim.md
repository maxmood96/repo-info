## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:b2ea9b75618e2d1754993b1e006f8ff0d8737d89a206aed752d7db1c762d40ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:098caf52b80d46033d2d615287ec247c33996ce1938ce0f7a95d0a56d772b18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233897774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9630d0aab5836f3acea992a595a5bbbccbb42b00bfbf051fbbea6f96f16144`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd24d9167d509c4a5d43ef17cd6308308bd9e06d98915114fb6ec3c2b29f3216`  
		Last Modified: Tue, 03 Jun 2025 18:24:16 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ed030dd7edb3cc85069377d9e3c24975c46debf9a25bafc0724cbc9cf032bd`  
		Last Modified: Tue, 03 Jun 2025 18:24:57 GMT  
		Size: 59.0 MB (59005831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa1bb37723c5f5d5ae1f71fecd27e736fac1f49b4663aba2b077b5c8ae43821`  
		Last Modified: Tue, 03 Jun 2025 18:24:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6642caf5d2814686801cb81353ecd77f3d38a1f48ac6283ae77b5acf0453ece9`  
		Last Modified: Tue, 03 Jun 2025 18:24:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73d9573fd761e5bd9ad585748ec7fd135ae5be64a7787853391adf727d51686d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5184465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f1a64030442a2bb0fc4dda831529250f58b7bca5062cf611de361e424b3b03`

```dockerfile
```

-	Layers:
	-	`sha256:fdb45f63cb08fbe9f5f9d734d7e3eec8344ce401518db36454883bf6ad16cebb`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 5.2 MB (5168586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9ed21565d75f806c49a32f88c099bb0b030fb121193c8c8fe102df84cbdac7`  
		Last Modified: Tue, 03 Jun 2025 21:37:42 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1fca19cf9b47b901834029c72c03dff8a58726015ae19ff0b61dda727474cc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231397618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736501021a8e3c56fccc088e7e458668712649e859f0147434cc53d23b0a6d9b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d42e8bebe42abc72f8a99347a686e6bcc371f4b39b9d2f706177fdfa30ce72`  
		Last Modified: Tue, 03 Jun 2025 13:55:40 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c47af6906c7f0f269134a317dc02930724d50b91f51582b85f47473e3215446`  
		Last Modified: Tue, 03 Jun 2025 18:41:30 GMT  
		Size: 59.1 MB (59137688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9d4886e5f750c950fa75ef6d705dbf8aaa6873b279afd5db31184d7812e49`  
		Last Modified: Tue, 03 Jun 2025 18:40:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059266713ce3bec39af0206ad5306ef624a81c8a46748983810d6b160dd062b1`  
		Last Modified: Tue, 03 Jun 2025 18:40:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f876cb51083a66da334ed434808a15e38180671a0260f0ba269af177d26e7aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f90f875098b02a52b1f60f86fab50669736093293d138c084207335eb680c4`

```dockerfile
```

-	Layers:
	-	`sha256:d75b77fa9ff9988fa5f227e6195c4da1fd952ede9b6c5c6b82a26999c6bcea87`  
		Last Modified: Tue, 03 Jun 2025 21:37:47 GMT  
		Size: 5.2 MB (5174318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7204a3f00ca61a33e8ce59f79c7a98812bde7e1082401f73c4b83f8666578843`  
		Last Modified: Tue, 03 Jun 2025 21:37:48 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
