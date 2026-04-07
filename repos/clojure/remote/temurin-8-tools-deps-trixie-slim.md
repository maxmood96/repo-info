## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:bcc629d67853291daa6d23b5381d589f09f7a9df8b9a8e7e90b37b68cdf51d4c
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
$ docker pull clojure@sha256:317914ce94f88af5deab64d9370e6770affdef2bade7e8afd36cf608d798da80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156958524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa681e9da199d9c2d03789520c39a1d2663247893c2e659dfce98e3657c8307`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:13:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:13:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:13:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:13:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:13:01 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:13:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:13:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:13:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eb531585f80630785cdb6193cfb62a9eb228fe297de6c6fd484e4823f50f46`  
		Last Modified: Tue, 07 Apr 2026 03:13:35 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eace562a06a3150a6e1e342761ac0066fc8e096b7df7ca1214cd48c7cad0a5`  
		Last Modified: Tue, 07 Apr 2026 03:13:36 GMT  
		Size: 72.0 MB (72012121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee1441b6826b4293e5707fec876d213a362985c434b806de5f473719ef338d7`  
		Last Modified: Tue, 07 Apr 2026 03:13:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42a90692574ad725ffc9748a685bdf5cd79d239104a72a1efc6e41ab3ab787e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83122d58aaa2e96bebac2d28434ebef5961422505e47757dfcecf0cae47cd37`

```dockerfile
```

-	Layers:
	-	`sha256:cdae01ee9941f37dedacb8c74d9c9683eefd7a7771abb9747890b29d7d6acd9c`  
		Last Modified: Tue, 07 Apr 2026 03:13:33 GMT  
		Size: 5.4 MB (5380125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49737a9541fd8c49d8613afcde5c37df6e85b034748894bc1ef8e2e1bddfaec2`  
		Last Modified: Tue, 07 Apr 2026 03:13:33 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2d111b78818de57ec86dae00b7889c7bfd38ae9ebd636c8719d1e734251c2593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156222247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4fdbf872ab2559cb45d2577bd38f3e591eef2c834ca5f86cf89deeb059e4d9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:23:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:23:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:23:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:23:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:23:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30436fd3e2e3651dd133cdc3ebfea015c368cf4e813db6ef2748756312c93112`  
		Last Modified: Tue, 07 Apr 2026 03:24:17 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e9528786f3982fc47d58bfad7c0b086061b82a31298848886178c627dad61e`  
		Last Modified: Tue, 07 Apr 2026 03:24:17 GMT  
		Size: 71.8 MB (71831428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfce6eaadcb3a0a11ac09102e54aeb3681eab75c413b6acdeeadb296ce50405`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90245a7fa9d7f1608683d5b885bf6c2e5eed21b176e33292e42523b512aa18f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c95eb135e2000ea0b2908cc34a873f58ff157fae95b1985e7e0dc123087890b`

```dockerfile
```

-	Layers:
	-	`sha256:1a659cf350f20acaa729c36f2a6c44a679af7dec8d0ea564c70c1cc3b1e5ad25`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 5.4 MB (5386594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e79faaae44b7ac3e93ff2508c1b846cc9db5c94a43ffb49c9c0282a7517152d`  
		Last Modified: Tue, 07 Apr 2026 03:24:14 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8577c18215f81e3dc33d03201dfca97e64e7ce29bffd3fdc93b93a58d192752b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163673803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42cdde4ee15e8c50f727ba12a4d4fc1fd778eeae0633ccd6b355a6ba69ecdde`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:08:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:08:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:08:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:08:41 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:14:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:14:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:14:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf4e66022f0a54019718e5fb82aff975c8ae1279a587e803dd7d8da942e46b2`  
		Last Modified: Tue, 17 Mar 2026 18:10:01 GMT  
		Size: 52.7 MB (52650377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82cc00d65e70e1d3a876d16f2f2407147b4e3661b569bf00c2fbe66a42d9cbf`  
		Last Modified: Tue, 17 Mar 2026 18:15:23 GMT  
		Size: 77.4 MB (77429945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24b651de48ab77e72296b181171877fff8b6264092c79f91ea7268daabb630c`  
		Last Modified: Tue, 17 Mar 2026 18:15:20 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47b781a99403d516974c6797a08fee829a17eacf8348cf8037f0c0fa0326b2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b838186e7ccce8cc3da2c020cda1cbb3aabd5ecb15705c6ed469ac42f71a48`

```dockerfile
```

-	Layers:
	-	`sha256:336a822085d8cd5ecb13ac58a2890cf15be97adb75f903c3d9427317ef11f992`  
		Last Modified: Tue, 17 Mar 2026 18:15:20 GMT  
		Size: 5.4 MB (5385091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904968eef104bc23b0ac15c0a8a670c969d50fc24416932a6c026faa69284c3e`  
		Last Modified: Tue, 17 Mar 2026 18:15:20 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
