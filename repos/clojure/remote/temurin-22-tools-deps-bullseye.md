## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:325f5ab5eb52c36082d1be0afa0c2e1b00f0d6ccce6237943151d8f115cc722e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7c1389dd109096e975103a3e05b8197f50741ec949395483b2f170bab8ed384b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280819090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee638ba9f131dccc4ce5f4846b39a7e237f61f29a3afaa5ce585ca1debf33f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15415bca63cf2af2fe9efce4349901ae4e4e5536a3632f29d4b9ac7a6815f933`  
		Last Modified: Tue, 02 Jul 2024 07:09:31 GMT  
		Size: 156.7 MB (156715496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c155743e31820f0c081a9548279ace40aee2121be50d2700732c8bcce33d01d`  
		Last Modified: Tue, 02 Jul 2024 07:09:29 GMT  
		Size: 69.0 MB (69021192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61577121c6099dcf7460a6e23745282cab2a3f66ee79d8f7d3d6dce050d7793e`  
		Last Modified: Tue, 02 Jul 2024 07:09:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da97fedab87109c3967c29858745f89003a63c942446c580f88f1e624a9b493`  
		Last Modified: Tue, 02 Jul 2024 07:09:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2008e2f5cf2cf11f57daa4025a781d25f45e55d819e0b045d47ba29b717c96ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5c599f57e1e5adf6f951098e49481b9b2433757007d1dc95792890d5ded5fb`

```dockerfile
```

-	Layers:
	-	`sha256:8cc098730d3bd7f6969ee318b35d96570ea488fa4428c6682de20276a3596f8e`  
		Last Modified: Tue, 02 Jul 2024 07:09:28 GMT  
		Size: 7.0 MB (6999784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2fef98e426b59b0732aa8d29b6d236fdcd8d9a3f714525464f1abbbebe6a5b`  
		Last Modified: Tue, 02 Jul 2024 07:09:27 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b95efd067ba39c64f2552b0006bec89633644e20c15f99729169ba3867f2619c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277593907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db248d8cc91a0087934165b5054eeb3287f5b7c2287dc76fde0e51127b7adb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a82e743f56fdd5686b4686e09264632831459e3e7ed605c7fff5bf27a78249`  
		Last Modified: Tue, 02 Jul 2024 09:45:19 GMT  
		Size: 154.7 MB (154738019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca738c59d7b1b7b0e62d5bc1f74fe66e8a83ab97772d9778ee904110a3b4f989`  
		Last Modified: Tue, 02 Jul 2024 09:49:17 GMT  
		Size: 69.1 MB (69133194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed021fc34d95381d029d83851f4a19e165d24d77648ea47c1ae5ec9bb1b11d2a`  
		Last Modified: Tue, 02 Jul 2024 09:49:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b1768addbd6401596d13e36b9d5c2f07147bea3c0c740ed5946126f16abe34`  
		Last Modified: Tue, 02 Jul 2024 09:49:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:88db20f54a5e3830fd0c76b3d9c43f3f9f38e954a748a24c9574f1301fcc9733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f65ef151c4e9a1ff64eefd50a8d202fc0612e1f906cfdc0f8ddd67db1e89061`

```dockerfile
```

-	Layers:
	-	`sha256:63c8dec7693948209677298085381f2686fa84153db4db881e6e18c90572a1e0`  
		Last Modified: Tue, 02 Jul 2024 09:49:15 GMT  
		Size: 7.0 MB (7005506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48540aa05a0448b47750121d05f5811c33943aa2dbf68cf7b925276da583cc0a`  
		Last Modified: Tue, 02 Jul 2024 09:49:14 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json
