## `clojure:temurin-8-tools-deps-1.12.1.1543-trixie-slim`

```console
$ docker pull clojure@sha256:799c673cf35f070a7e2cc1cb6743ee35bae1cf6a31ad19770ae02e585a8ffe8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1543-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0bc5b8a5bc7476d14341b5932ba557d289951a6efa409cf12de921c7cf13785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158918276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5899e2aea4ea6f885753007ecd8ab5d9df6f7cba785e4c7d50453ea5e9db5edd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3027bac347196f3028d06f80221ee420e9ad855e5c00339bbfa0557a9ae2305a`  
		Last Modified: Tue, 03 Jun 2025 10:33:22 GMT  
		Size: 53.8 MB (53830502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea38652695742dd05a8111c35a676ba167baad52ea42b608b1cb81ac7df803e`  
		Last Modified: Tue, 03 Jun 2025 18:31:57 GMT  
		Size: 75.0 MB (74967674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd4efec434a5a02d8708cf6e242f8fb6d07e48ee4f2a89575d5992244bdefc9`  
		Last Modified: Tue, 03 Jun 2025 18:31:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1543-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d77156d2e33256128e62da5c578dec0a7c714b29acf9f4f70840ab7b20943885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7c607196ea10e84d83ebff1b4d135d632648f3c3bb671c2c9964c2dc0fb4a`

```dockerfile
```

-	Layers:
	-	`sha256:234bb49d96e9fe21895b9caa9f550f713a6523608d5b7cbb1af11308880caa60`  
		Last Modified: Tue, 03 Jun 2025 18:38:31 GMT  
		Size: 5.2 MB (5240142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd316c781043a50dc37ba0ea5ee5a288b2fdd548f46e1723158f96e111c5aad`  
		Last Modified: Tue, 03 Jun 2025 18:38:32 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json
