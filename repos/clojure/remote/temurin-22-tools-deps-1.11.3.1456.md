## `clojure:temurin-22-tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:29a870bbf11765a8d007f8c1d4864b9d5a3d6f93d899afac99349b7ae808a889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:0a479abb63b45e244570ce8a4a2621f3fa84bb25179ab49f0f855921b5d66acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286586790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be43ab30dd9262d802602e915f3d9fe43c83bb0543daa5e752a4f786d6b30591`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447b658c5c15949a03bc2528d46d432d101064b4cf105f06701426174a9128b`  
		Last Modified: Wed, 29 May 2024 19:58:21 GMT  
		Size: 156.7 MB (156715503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb0a4bd5567886591fd3a13be67c563ba73f15e4d645a53cfa923bb9e7445d`  
		Last Modified: Wed, 29 May 2024 19:58:27 GMT  
		Size: 80.3 MB (80293847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5bd1c08bbcb19c24ab1bed8bd8249b2c494ead383be85563ccb290cd895d2a`  
		Last Modified: Wed, 29 May 2024 19:58:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde85bb5e234ad89fdde98bf79716bfff51223e549d972ac18ca83c6648b6a1b`  
		Last Modified: Wed, 29 May 2024 19:58:25 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:cc4d26c362d91248696fb43ba2a3705721f54d9649149aee9baf939b629568f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6977419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc00cdc1c7ba674779477ea87656ba9ab432fcbdb30bb5adc8caeb8cb1e8bd70`

```dockerfile
```

-	Layers:
	-	`sha256:3580d6abfe8d6ed507f5cd48ea6be0c796589ca96c70044f8e6916945955b0f2`  
		Last Modified: Wed, 29 May 2024 19:58:25 GMT  
		Size: 7.0 MB (6961345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5de19741f9bca2a0a11104d289d79d1076c4a0a98da6ef83b8712b4a575568`  
		Last Modified: Wed, 29 May 2024 19:58:25 GMT  
		Size: 16.1 KB (16074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8606ff04291ae4f292da3143591dd4229744f55e285db231a41754a4821238d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284397375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa60dd729fdc428edb81c7eab0faebf74a525baf3bf07ae99e4c2b66a4840dfa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
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
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108f143689701d7a45796937e60c77f7cbfbb3549865de2a74d02c7a13faa376`  
		Last Modified: Thu, 30 May 2024 01:38:23 GMT  
		Size: 154.7 MB (154737940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a79e4366c7358c331d29541a6c5f9d5fc83865e249d2787340a9184221c42`  
		Last Modified: Thu, 30 May 2024 02:06:29 GMT  
		Size: 80.0 MB (80044998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdaf1295182ce50043f2b841350b62a7426d1e8d81dcffa7c21672be6ff8815`  
		Last Modified: Thu, 30 May 2024 02:06:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810290c97a3b90aed1e7e5f43de2d4ba2d2a47c087faab950ebfd37afe01e3f0`  
		Last Modified: Thu, 30 May 2024 02:06:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:46c4826e36eb1e2fffbdfb62e3845d332f47b1a3a1fe9d9418896c74f7096f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d82d7f8d1b06e6878a404368323571d6f688f7e52c177f71a7dbabaa369140e`

```dockerfile
```

-	Layers:
	-	`sha256:80c40aa55d6b89319de9514cb79dae55f69e2cbdd3d0445ce2737ceb8285dc12`  
		Last Modified: Thu, 30 May 2024 02:06:27 GMT  
		Size: 7.0 MB (6967756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c564e3952213ef18178b6daa181481796b2030b8f5cb0bef057ad61295f07fd2`  
		Last Modified: Thu, 30 May 2024 02:06:27 GMT  
		Size: 16.6 KB (16634 bytes)  
		MIME: application/vnd.in-toto+json
