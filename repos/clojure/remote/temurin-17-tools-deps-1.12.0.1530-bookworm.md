## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:4252af9a7368ea2dd41d2cd9f247f157eb252d3f3d0b6e0a7d293a96dd99aa25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:930f58b55ec6b73b86c1d49b47765d9cc4a7d57ab4a497b8dc49034aad1a1f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276427632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f9a871e33ee1f778cc851b6d0fc84f8697d362cba105a019cd424900628d95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027fa4fdbd35d8eca059a3237e4c146646dd29d2da3a6efc6b5b16c7a99d3f3e`  
		Last Modified: Wed, 23 Apr 2025 17:19:30 GMT  
		Size: 144.6 MB (144635075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377126c762581716b4b2642134620ce330a5681e84f1b4bdc00366f69c8ac13`  
		Last Modified: Wed, 23 Apr 2025 17:19:30 GMT  
		Size: 83.3 MB (83300971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48844010d592ab4b51f44a7f0c01e1550337f61630a6629eab86de55b38bd9bd`  
		Last Modified: Wed, 23 Apr 2025 17:19:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d46c676bfec78b5194f02c3a20846784ba9865a5e00a518fb73338b6399074`  
		Last Modified: Wed, 23 Apr 2025 17:19:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6ff429b5d1dfa8193d0e10c30c87d9f5db0fbb828f54b588fd604a9b6a95759d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7188297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6411d9c5984ca10d8491c972545d908add03d7ce57ea4d1b18f20260d11bdb`

```dockerfile
```

-	Layers:
	-	`sha256:ee4f4f08ab1b2f32b1b6ad18e995db2b7a19ec33153677776a292c1b8d0fd8b2`  
		Last Modified: Wed, 23 Apr 2025 17:19:30 GMT  
		Size: 7.2 MB (7172476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69ec8b73fb218c1ca3506d7683fd19cb2f4720c89f605db3354f114f9b2eef9`  
		Last Modified: Wed, 23 Apr 2025 17:19:28 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f16bddfcffe9239eabeb9d3ea9e29a7d0f5cd37f969bc55f735b49394cd79b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274959778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005e301fd2fea2adb13f5861b3035aa5e67dddb941972cd1c0eaf93123438a21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7185f5fdf0b4c7dbff6fc01724356aea3a8a3b03a4107b5252e6ba0d7c3824`  
		Last Modified: Wed, 23 Apr 2025 19:45:21 GMT  
		Size: 143.5 MB (143512628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043c5e432952a2c3b39ca9e9c6cef87422509bfb51a9aaf73987146604de172`  
		Last Modified: Wed, 23 Apr 2025 19:50:04 GMT  
		Size: 83.1 MB (83118637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a50ae0f4bc1026625fba66f130c3a7566ed443ad5a00d55402807b433a24ee3`  
		Last Modified: Wed, 23 Apr 2025 19:50:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d362ebf4cde11b4558860aa3cec723352572aeef3a5903cf4a5a4f5bd952a7`  
		Last Modified: Wed, 23 Apr 2025 19:50:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f87bbbd5a0d4b18a33fdffe9ec794c7309dd1bc9a269b2157431a84160c455f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe318d2580f4d710b590a4cfc2a1a85d822d4a01ded2fa5d52d327b5dcde80c`

```dockerfile
```

-	Layers:
	-	`sha256:ba33eb71835adc1ae35c5a4c2af0492706da4943499ea9bda7becb5d036e5aa7`  
		Last Modified: Wed, 23 Apr 2025 19:50:02 GMT  
		Size: 7.2 MB (7178239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac5057ceb8e4634b492a67fe64c7e3ac323971334567c7dd38a2681dfe092317`  
		Last Modified: Wed, 23 Apr 2025 19:50:01 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
