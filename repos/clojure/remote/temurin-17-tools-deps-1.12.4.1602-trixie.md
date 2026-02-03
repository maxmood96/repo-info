## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:25216075993cdd0dc0175ce424ab37df2f3275b3c4ef5284f57665977db23b13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:77308d9aeaac0849012c5a2a2ce1a67cba3639fdcada559c61dd700ce6edfa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279684188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432caa8483055ae053a77c11d61089f6823db3965c335318ba69e09473b2912c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:20:52 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:21:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:21:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:21:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:21:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:21:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6b5ccad96566173b43229caa3526f8d98067f8d2d3abf1223de66ebd02e5a9`  
		Last Modified: Tue, 03 Feb 2026 03:21:36 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437a15311489559bf31d5fcf08383cdfb4d3cce33dced587ff64e6bb58d84e9`  
		Last Modified: Tue, 03 Feb 2026 03:21:35 GMT  
		Size: 85.5 MB (85542286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddddf92f3e9c9d880dc286b702ccd4ce70424162e11e6508b3e9831faef5138`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee16f5dc0e7137c908d078bbd959a5e5df69e64a31334b37766aefb392b0256`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa7e14455fd455ea34c1c3b8914e9ece34327e9a71b69a405f66b8a0a0112242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa580b3ee31d816630b42ab9c810c044fc8cad2900f0eb135a51b47913b790a`

```dockerfile
```

-	Layers:
	-	`sha256:0f45fdd2024b07a38bcdd1e079729d851e68a85a6266853fe483ae61870e6ac6`  
		Last Modified: Tue, 03 Feb 2026 03:21:32 GMT  
		Size: 7.5 MB (7467828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420eb8a873a1c73f1fe2d4cc073ad09c6ff7b9a768b9ccfa5f2f33836831a130`  
		Last Modified: Tue, 03 Feb 2026 03:21:31 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3470730190e0a18974cbe348124ca3fc919f20368cd8eebc2ea8eda972f9df43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278694122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22ac080c201b7fa88daf53157924face58edbf2408d071a60aa0589ed5f8f06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:21 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:23:21 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a9f0a030353240ddda4cbcd483763b021b00b4088b29b17ab8bfb24238bf3d`  
		Last Modified: Tue, 03 Feb 2026 03:24:02 GMT  
		Size: 143.7 MB (143679921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bb5d1dfda71e663f7c3c02ef17752eddc6d424e11e0559b6c8844053d3fb9`  
		Last Modified: Tue, 03 Feb 2026 03:24:01 GMT  
		Size: 85.4 MB (85361139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b48dc019008523f7ff0aaaf808cc1ca5543a70f4bb73f8ba1af3d11d3ab3e6`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088fa2c40b1d5e122cd04ee8db1830de236086363891508fc2eea83ab88f28c0`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71bedf68c074a42371efd16fe60e9f763442aedae62759d0b0d78a36ca1a3a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0464420f45af714186513806e2964f829cf30484f8651ee94444b94a2e0c973d`

```dockerfile
```

-	Layers:
	-	`sha256:8befff019ea730dfee61dd9bc6805786d3973a7a999c6c04073ba401a73c3c85`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 7.5 MB (7474858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29651c02e99a77868e5fa3d13175b851d341e4c38d511c73dc664c5a825e0c8`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:91a197121b78949cf65fc047ad20e133dd15774214e774ac73e5b1e9eab91d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288585356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddcf1f66c22322ee11c2e7eb21d725b6ed718009ecd7f7e6426fa5f282f7952`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:41:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:41:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:41:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:41:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:41:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:45:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:45:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:45:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:45:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:45:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba372745a3f66503d172e659feebce952b517e572b656ca7ad4427c81440823`  
		Last Modified: Tue, 03 Feb 2026 09:43:13 GMT  
		Size: 144.5 MB (144524726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03b715dc4f73858aa1c4e67671945edfaa99cdd950bd2cf99f0d3d665780a0`  
		Last Modified: Tue, 03 Feb 2026 09:46:55 GMT  
		Size: 90.9 MB (90947469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1beff8693dc445ce4cccaaf2caadd3e95dd9b8bc42fd3843a7bb9a20813374c9`  
		Last Modified: Tue, 03 Feb 2026 09:46:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e244e865dfde2dc15dc6569ca018d01094377bf977902d25166781cc5f4d0861`  
		Last Modified: Tue, 03 Feb 2026 09:46:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d7ee8b22db1dbfc9d52b54a46783522ec2eee6173bf345a7019c57b901d94994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812bb1eb93ab7a549bb04e885c5e9ee84616844b8a923a430584a8dee7ef3610`

```dockerfile
```

-	Layers:
	-	`sha256:38520e364a001d1f59acf959c6813a28eaa85aa41a941fbdf5a08ec486fae290`  
		Last Modified: Tue, 03 Feb 2026 09:46:50 GMT  
		Size: 7.5 MB (7472249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb24b2c2221a3c152576c64861925030453e597283e76d47cf7630092af48ec5`  
		Last Modified: Tue, 03 Feb 2026 09:46:49 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ee89d285b4169a172a53f40849e97d89c51b69d3445729fda8d4a6350ca724d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270726822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5860ae589ff1016a15e328d259c7c42f1b164461e3588c03e8b6210f4d43cc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:02:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:02:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:03:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:03:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0521af9429b24592bd981b694df00f2d02ab05a0bbb63192b66fd3a113c887f`  
		Last Modified: Tue, 03 Feb 2026 05:02:39 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e4bd1e22af93d28689f0ab20120c5927d2fce6f2e55a11c719edc1fbcf065`  
		Last Modified: Tue, 03 Feb 2026 05:03:41 GMT  
		Size: 86.5 MB (86511632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d412261b3b83a828dbb590e4b722bc164306d24e48ad849a2c46308cb348675`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c96c69f0a4832d4fbe8b9f450d66db97b808dbeebfdc1e473778b0f562fcc55`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d40e4b08b2cf917f90b2b5b256779a46507d1a6e81cae55055ee97444bb39024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d015407a3ba71296a11b7c6acb745432f599d6492590c300a84c4172abc900c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d72b51a75250e065edc9e5309261d1f2ea25c5efb6522ad2c47ed4bf77629a2`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 7.5 MB (7463750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3594c17612954abcda742be695766d4e04bb07c5f1ee92737f0ff02184c1248a`  
		Last Modified: Tue, 03 Feb 2026 05:03:39 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
