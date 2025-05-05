## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e56314679888c2c6b53da555a2ecf0ea91d7c2474fe9b5a5dede8b9facbbeed5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:14686bfb41dbef14ea903478544760858f0c04a0be84e56cda2315f6da29d690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233883511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575bba59bf2a9b7a593121aa3f4175a6ae2724d5b45daec5333ad25f83526bf1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffeabfb2d9fc4a0c541374f73caf24c5230cd0fc3931142e91473df8f662723`  
		Last Modified: Mon, 05 May 2025 17:07:36 GMT  
		Size: 144.6 MB (144635029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08c06b9df357b383af104be063e20245df5e89451c246552ffd32f390b6e3c7`  
		Last Modified: Mon, 05 May 2025 17:07:35 GMT  
		Size: 59.0 MB (58992840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f22f3da9895ce82dd1ca46b6928edb34c2194d2528800e368f838423e26b6f`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d29b4ffff5f1cba3c911fba8e40639361f481b409cb0310f418ec2ab05f09`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b600419dbddc5e516065b03310e9f241a3db9d8d662fdae13c286f39210906e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc76b8b541c72569515b96e94b63fe9d76796228942701de04bc95fff0213c5d`

```dockerfile
```

-	Layers:
	-	`sha256:cc899bba178f73ee0db07e9e793fed60f2286a8225b6e7f5cf6deddaa4f969f3`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 5.1 MB (5119067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b0b2f08f2bc880f438f8207eaa5a05bf57d514f5303c586493237bce56af08`  
		Last Modified: Mon, 05 May 2025 17:07:34 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edf879da1e870f59daf270d624ed9f3baf3a3077ba6679a402ce6d710d565ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231385716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebeb2ef797d3d11cf7258e6efe6df9b2ba59eb571eba340ed6b19fdea78410f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72262fe32b026e7f23e9a38bfb2a66973be30355ac7b2a0fe73a91bfb575d0f`  
		Last Modified: Tue, 29 Apr 2025 20:15:14 GMT  
		Size: 143.5 MB (143512633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0e19b5e3394bc095f8ad5c27d5c5e1c3fd22b4f6cd80b767e30c4aeeafc227`  
		Last Modified: Wed, 30 Apr 2025 01:35:49 GMT  
		Size: 59.1 MB (59127401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e0548c3b863fc08614dbe860fdd2fc9bd6df7bc66e74b6161d816eef40680`  
		Last Modified: Wed, 30 Apr 2025 01:35:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429f73077911a0c66230a5e31b6a230afea1fb6be9b70c1a51ad0dc0658b580`  
		Last Modified: Wed, 30 Apr 2025 01:35:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a808735d0085e0ee1d59a020d4b64112cd6c9db272f5339d4cb8923800567054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b302d681ec091dc9c289025aeba7a10cbab2e20726c51609c24f3a1508c442`

```dockerfile
```

-	Layers:
	-	`sha256:5e37b241d0f0a1e98a24ef6da0ad8f7d048dde6d2c710d69a2c5a66faf5ef57c`  
		Last Modified: Wed, 30 Apr 2025 01:35:47 GMT  
		Size: 5.1 MB (5124799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b297d6956fe648b368f3cc30687c20d8b631cf4c1823cf062e74ac2b35e6ba9a`  
		Last Modified: Wed, 30 Apr 2025 01:35:46 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
