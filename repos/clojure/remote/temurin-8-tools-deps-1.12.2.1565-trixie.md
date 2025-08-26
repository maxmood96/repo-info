## `clojure:temurin-8-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:e2657558449857e7927b9dd4dd904625179367a9a1db4c367f25f69b6e8de623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:49061fab94ad9635e0b5dd79e49c9b19d2f3fa5c52cd8d24d8c5cb205f1ddc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189543434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e349bbb40d178592a9b0299595595d65253a8f23e69baaeed0207ddca86e93`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a34e94ff3c52086b9c3ccadd203bf4632a9eef5079c0fffb7dfe95735c6e690`  
		Last Modified: Tue, 26 Aug 2025 19:18:08 GMT  
		Size: 54.7 MB (54731336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739f5c39c79c9506374f69005f71238d256efd03228d04d0f5c389f471b35c8`  
		Last Modified: Tue, 26 Aug 2025 22:12:58 GMT  
		Size: 85.5 MB (85533171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6090005fe82541d2c7240f934114f3e5e817c96898f8cf512c2dcdf1744c3e67`  
		Last Modified: Tue, 26 Aug 2025 17:28:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7598bc9f6aec5dae05af735215bfbcf043f94743705522a74edec6bd4c316c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1437986aab64dfe8405879c993e2debf5fae2fcde9ff04679e901535e2661dd1`

```dockerfile
```

-	Layers:
	-	`sha256:ca708f3a21264ed1a9a82e185a0924a03bd8d9db8e3ad5d8a3532a612727f558`  
		Last Modified: Tue, 26 Aug 2025 18:44:57 GMT  
		Size: 7.6 MB (7583831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a757cac0a2b9c5d01a2510a713001f09cf283aa14e0979bc3bbe01951ebb47`  
		Last Modified: Tue, 26 Aug 2025 18:44:58 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:64cd77c59ca61501c76764dd0f1d31faad2844174df05be90f58ddc517878622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188834469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243b2857f37e046009c5a2fef7d6a80d7a3fab70b5e9a5f55098fd4859786bed`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d601e9520efa7df3d63d77147625a058590324ed389fc928416c360b90f26b5`  
		Last Modified: Mon, 18 Aug 2025 16:58:11 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532f3467bd0865c3e593937afd852b73e24b8df17dc0c180d60e37d46e43f68f`  
		Last Modified: Tue, 26 Aug 2025 17:33:28 GMT  
		Size: 85.4 MB (85356612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fe79f4ee0fcbe15552e45a9e725cddcebd8d83e5c75feffbb3566fb5d24f18`  
		Last Modified: Tue, 26 Aug 2025 17:33:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05dea62b0e8a65c541fa49badbed23ede3b99aa238e471c6c34da9b5d23302d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24304539d621bcd2ef9ba3e00c0036a8d4d45fcbd13518d645ea2e0e5a83429f`

```dockerfile
```

-	Layers:
	-	`sha256:36f3590e8deed3d1c6890f7d27dc9267b00af3d404a8c8c03df15ce1560021c4`  
		Last Modified: Tue, 26 Aug 2025 18:45:06 GMT  
		Size: 7.6 MB (7591559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28cda8d4a299555cbfe46958169aecb11fc8b526cadede11c575bc98a18778d6`  
		Last Modified: Tue, 26 Aug 2025 18:45:06 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0ed0db6a18d1a3d9ca27d4e8d7475da4f4a235bfdbe32e15acd813f40d5b1bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196210944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9af5c22a7d53f56864d93e6934fa6f4f060f9eafc4d3a9e14c6cb921a1167c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959807e042cfcaa6a6f91ac803622b4131aea7366490c83817cc1b36e2a904a8`  
		Last Modified: Mon, 18 Aug 2025 17:05:01 GMT  
		Size: 52.2 MB (52165401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b8f4b03b994c732b6313d31f8f3ccf2168ee6a259c9fa17ac9c0332b53370d`  
		Last Modified: Tue, 26 Aug 2025 17:38:09 GMT  
		Size: 90.9 MB (90941514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b57a5b014d2daf0e2751c59332cb812de14c6e4b5c5d6a50cf091af0b7ec852`  
		Last Modified: Tue, 26 Aug 2025 17:37:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a39f5c9936750ffc32056838e79b84e400bd67826c6ebe02bd1cdfd83c5ff73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de63e81953f7f4f40a17cc7b0655a4733d26cc2955fec9c6a22e7f4d5509e86`

```dockerfile
```

-	Layers:
	-	`sha256:59d4b985cf90953adc3d2f4fcf3a634389933f4ffaf62fc0732f9dee6a7b6808`  
		Last Modified: Tue, 26 Aug 2025 18:45:15 GMT  
		Size: 7.6 MB (7588843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef0385d2323827e5ee0a921a416aa9f8eab9942988b585afb66509b17687061`  
		Last Modified: Tue, 26 Aug 2025 18:45:16 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
