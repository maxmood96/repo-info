## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:ba3a85bd22035d5baef5569df6f40388f5f3e8cd356a6face8502b55b3bd7782
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f3a77a2cdc9b919a9b4e955592abcf62473fc1d41e2710d43edd397826bfb309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159137067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a947503cfa6d9277f904ed75e229e09e0dacc46b082b3412732665ec74dd129`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08cf07e3d5c4a5eb6bb2062e4080a121ac9ec6f330fd8dd61de9e97556be865`  
		Last Modified: Tue, 03 Jun 2025 18:24:42 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc56eb1f96ca71679ade12da4452f128332544d1d304c6d0c630db7eeb62c8b`  
		Last Modified: Tue, 03 Jun 2025 18:24:48 GMT  
		Size: 74.7 MB (74664862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e004251bf5b2fdf53afd9c5d63f9fb60584896109f1a88ce739bcf927d550bc2`  
		Last Modified: Tue, 03 Jun 2025 18:24:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:faff795d0ce5dce9209e43315a3f15f7fe3b1dd5d0d4cec9ff33066a66dd25cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f863624057abf76bb21c60939ea9d04dcbc1a13ddc357f783bf1f9a4656a6f`

```dockerfile
```

-	Layers:
	-	`sha256:a165da1c43472d33b410d7f421ba86ee413d6ef2adaf3d7b0dd6ca178538148d`  
		Last Modified: Tue, 03 Jun 2025 21:45:05 GMT  
		Size: 5.2 MB (5233675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f99a124f870300e550f07d213aac902dbae625dd6302eece55a68532b5095bb`  
		Last Modified: Tue, 03 Jun 2025 21:45:06 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

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
		Last Modified: Tue, 03 Jun 2025 19:21:10 GMT  
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

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bd6443320f91aebf01aed1c6037049894d77af3dc1adb7e3cfa4f97e1da32e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.2 MB (166150814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d638e551ca843d9d077efffead0b851f1877f54f9c9c0fda8036584c79a9b7d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed347681401881a3761af3b137e387f41b112bad5ebb9315d39c8eed38c8394`  
		Last Modified: Tue, 03 Jun 2025 08:12:54 GMT  
		Size: 52.2 MB (52167965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afe9bf93747933609c237f0e89aca48f07795a1cbae3acc7c5eb4c0a4c2c739`  
		Last Modified: Tue, 03 Jun 2025 18:37:47 GMT  
		Size: 80.4 MB (80401640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c189c457a28c313f8f76885cfe81ed9f457e6554161834af34ce442ddcaa2958`  
		Last Modified: Tue, 03 Jun 2025 18:37:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:518e7bea33d103fea6b30d035b332919412e34b60646875aaaac26536c975793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5ba7891189186c061726d2a216d78c6d1a5f6054f29b045ccd56920e21c72a`

```dockerfile
```

-	Layers:
	-	`sha256:82ac47568dd50fef1b7f4ba920bed2744ebbf102c791dd9e0f41808246b4f0d5`  
		Last Modified: Tue, 03 Jun 2025 21:45:14 GMT  
		Size: 5.2 MB (5238639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aaacb0962a8741f710bea3f85c9b0312eb2ee81b00a26a28c1c0652b6773baf`  
		Last Modified: Tue, 03 Jun 2025 21:45:14 GMT  
		Size: 14.3 KB (14318 bytes)  
		MIME: application/vnd.in-toto+json
