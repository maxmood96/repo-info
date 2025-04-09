## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:811692fb855c71e289f09cd727da1aed6de640d6e9c507c21699a1d15c242223
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:48e58881bba10f0f41490dad77e51746a0860b1457241932d2cfc66bb74df6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219434903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e521fd926e94c7dd252c62949dfc4b7dfbbe858ca31249d5a3650c4df9ce21dd`
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
	-	`sha256:21fc9975e7fad3704a55fdf6228e858326023062a058bb7a21c728ea0a2963ce`  
		Last Modified: Wed, 09 Apr 2025 02:19:34 GMT  
		Size: 89.9 MB (89949048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f792f6f78ef80cade9bb1d3200f2e8c38625a83c1df7ee21f410aa9d239c59`  
		Last Modified: Wed, 09 Apr 2025 02:19:40 GMT  
		Size: 81.0 MB (80994272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce02f9a39dc3c6a67f21e0efd73a16e0702a3cab0df7a694019891008800597`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155fddfee57acf1316d5468c7bd36c79ab8808b932992d3a68d44ed9a8e48bff`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e99268cff7a0cd3b7d45b81f3db761c68bc6c8aff8c689d1a0d49178eb16cadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f8b3c14a9fb37f0869d27e55dc149b77d967e0b84644cde59394e38f3d8b20`

```dockerfile
```

-	Layers:
	-	`sha256:81a411852027d3c1ad613579245319bab6ec174daeaae66b326e65bfec98127e`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 7.1 MB (7123792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0827cfe4b60a8b94e79915e2d913191541976b332044be00849b5e7ed6c01d82`  
		Last Modified: Wed, 09 Apr 2025 02:19:36 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea542ae9c415d6904d9ac9cc47de791dc5e46ca29696bbbd15b4c1003091b017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218263543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efcf01e317eb1e964e9a134230b45b99e02aff3364a56c952728f17c73dc1c1`
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
	-	`sha256:e663ce4f306cc9c264ec0b57d4f93f02ea679e43515d91dd37eeedeef5a0293b`  
		Last Modified: Wed, 09 Apr 2025 17:47:39 GMT  
		Size: 89.1 MB (89092703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec298afa41927567bcbe86ba58bec0327f44d0bcbb8a13e99bcfe11e69b6d13`  
		Last Modified: Wed, 09 Apr 2025 17:52:02 GMT  
		Size: 80.8 MB (80842329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5894df7e8b74f10af94b07b2a49b2a715d3c86fb124f85b25ba4f5bc6a1063dd`  
		Last Modified: Wed, 09 Apr 2025 17:52:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb8f83eed9331d2cbcd240fdd2e0d510c1a1d5af6583ed9bb4d83181b2ddf0a`  
		Last Modified: Wed, 09 Apr 2025 17:52:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a099da8d4661a7d4f957b3bcbaa89b0f74f87bfb238c322e1995047778acb6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dab4bc8ebe15e314befb59559ff8c5a83ed84a0cec72f18febe1e2db085a`

```dockerfile
```

-	Layers:
	-	`sha256:84038d680776a97d1bd995c9de3684b550898a3f06fb459ba9d794ad2ded2487`  
		Last Modified: Wed, 09 Apr 2025 17:52:00 GMT  
		Size: 7.1 MB (7129576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81769c9fcbaa6ec10c3c8d93f5c67aff22b5f1a6f6bfbf172e9626088dd6fe3`  
		Last Modified: Wed, 09 Apr 2025 17:51:59 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
