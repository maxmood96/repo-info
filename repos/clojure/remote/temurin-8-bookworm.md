## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:4b8de141e0c2cb6cf831ee4f402056f143a6fb076c50c1fe1caece3b7df048bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:64a85e7e387670f8ebf0b08ab9a567156ec2f334e767e6f5e17e069345051337
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233652026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15087d66398e8d633342ec2228dcae3831010b3fd618a714e3c62d2358dc8194`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:51:42 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:51:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:56:24 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 11 Jan 2024 04:56:24 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:56:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 11 Jan 2024 04:56:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 11 Jan 2024 04:56:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ee0cab5ab6aa98c37ed3fc43d77bcaf83ea4c8a69ec6d510ecb9e0057ee49c`  
		Last Modified: Thu, 11 Jan 2024 05:14:21 GMT  
		Size: 103.6 MB (103598285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f84159ae89c1e359b18eebd7cbd88a5cbbc0f44136c9ad8bb4b8194b840157f`  
		Last Modified: Thu, 11 Jan 2024 05:16:13 GMT  
		Size: 80.5 MB (80491635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd6934c571f2706bb43108bbd22fd533b1e58e1e74e4ab812e334c7bcc672a4`  
		Last Modified: Thu, 11 Jan 2024 05:16:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f2cbe123762b058f388404629afcddce517750f99494fe7f946c9accb193e93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232548861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c71793427eefb2c5896fa93aec18ea00267f7bfde627a625bcb07a61ee9e8f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:54:25 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jan 2024 20:41:32 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 04 Jan 2024 20:41:32 GMT
WORKDIR /tmp
# Thu, 04 Jan 2024 20:41:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 Jan 2024 20:41:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 Jan 2024 20:41:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd83395931034d8cc43b9c1210837008aa4d9f602c045c8c2f80b89be5b9e2`  
		Last Modified: Tue, 19 Dec 2023 07:12:44 GMT  
		Size: 102.7 MB (102701533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240ad40809d4c18da1bfe09513e5c277ef7250eed4ea3e2176ca9d1a0fd1ac60`  
		Last Modified: Thu, 04 Jan 2024 20:53:16 GMT  
		Size: 80.3 MB (80254450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d193e2556ab0188695bed1dfc93ea86b9a0686eed6ba92bd4d380df344ec9db`  
		Last Modified: Thu, 04 Jan 2024 20:53:06 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
