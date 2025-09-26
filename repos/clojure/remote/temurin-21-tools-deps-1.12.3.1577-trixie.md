## `clojure:temurin-21-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:cfd6fc57b079ebd1050f4ae56bef621b97de33bcab0c2b8c143a84e026fab864
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

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:17305887c7e60259d1a564598e5acd2e9b7d7f86e5b5908a92c8a64129bf455d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292626332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e2b5723c67a70633c3d1e955233f42066591f5b969ae83984e7ee198b0890a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d151fc70160346d07064bb1975b73f49d0ab8cd6551f01dc08dc4c7f3f9fdbf3`  
		Last Modified: Fri, 26 Sep 2025 20:02:32 GMT  
		Size: 157.8 MB (157804727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133759d7ff236c860519dfe2f6fe3919bae1b081d16c1ac374e7e9e7bcad302c`  
		Last Modified: Fri, 26 Sep 2025 17:58:27 GMT  
		Size: 85.5 MB (85541033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e71d8e5378caef9fb701cf785d41294310024d874c823a4d69fb3d835336e3f`  
		Last Modified: Fri, 26 Sep 2025 17:58:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6b660e0fbeabe12790c6cbe2beb8599995cfe64e877a4187bb8d9754f42394`  
		Last Modified: Fri, 26 Sep 2025 17:58:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a9ef1e0c3731660fa5d27d2a8c07a2bf493ddf5688102eb3d9d6346a6f0dea07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6b904eb863693fc5cb8ecb1927e25a806f70c2ec8aac84a4b508fd425af507`

```dockerfile
```

-	Layers:
	-	`sha256:68058133631e91fbd93a987001eb0a99f3e340499da6692950bc183837647278`  
		Last Modified: Fri, 26 Sep 2025 18:42:43 GMT  
		Size: 7.5 MB (7469947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d1cdff898f2c4dfa4d4721124496a771a335dcaf4f3a9aafe29c8b86faa1f37`  
		Last Modified: Fri, 26 Sep 2025 18:42:44 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c5959f0f34adc6f912d31dbb35cb93009072e96954a5cd55bc212966304b2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291089366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e0f9e43b574b88222a9435273f1d1a2982190e65d19d6ce9c2f0d5d661f1ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dec167ae266d1a810b373c0fe05aaf32e2357be2cb8ab447e10ea488c88e61`  
		Last Modified: Fri, 26 Sep 2025 20:02:04 GMT  
		Size: 156.1 MB (156081152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1170dac22821b882d99c9226f7f18d6061c2e6c5519f6333faa6a477b29d7c`  
		Last Modified: Fri, 26 Sep 2025 17:56:22 GMT  
		Size: 85.4 MB (85363426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094f79674e59e61ad6dc45bb9209b1184284f5cf7740feaf24e844b849754725`  
		Last Modified: Fri, 26 Sep 2025 17:56:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a7ac7c133dab603fc15bf38d8f3cfd19817cd41e9e2f5098952ebb13c76c26`  
		Last Modified: Fri, 26 Sep 2025 17:56:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:decfb7b35967f4e3d80ac507e6a4e7a8bb32e7210d3b6532adf6558e3aaa483b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991584270ea2ccf6c1036c103f8ce105b9d92c19f2a192d42cab274f435eb087`

```dockerfile
```

-	Layers:
	-	`sha256:9ec71aa3fe4042b626c460248fbae7a88de4ffc845d80f302e264be430e879b7`  
		Last Modified: Fri, 26 Sep 2025 18:42:51 GMT  
		Size: 7.5 MB (7476977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c5860352ede2f52432f0f1a1d8abb206cccb92f8e9d2eb9beea101f519ba4f`  
		Last Modified: Fri, 26 Sep 2025 18:42:52 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1728766f6a9c8f39b0d4ea84887dea49a97753faaaed053965e3d713f0c5c58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302017158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19f74d09ffe8d51f84220300de188a70ca1f3f22744c963f0cbc950da1c0c15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330554e28470024f1db371837c89576dd6d42feba85f739f013830e8d15b7103`  
		Last Modified: Fri, 26 Sep 2025 18:28:53 GMT  
		Size: 158.0 MB (157963450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a1cb3469fd517ed4355e94b00751e21e9370954a75627abcc35dfc564486eb`  
		Last Modified: Fri, 26 Sep 2025 18:29:08 GMT  
		Size: 90.9 MB (90948232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bfa4d10eb5df9bec83fc70598e1717099ee8eb82db07945b90b811451e363d`  
		Last Modified: Fri, 26 Sep 2025 18:29:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89efb1597c315cf783bc6ddd4b07088ec01dc47b7aaca8a926f7c00a2ccf4637`  
		Last Modified: Fri, 26 Sep 2025 18:29:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40486cc4f0c652db446f3853d99900eb082ecfa038630d743cbdc515fec55180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6afbf95a84734074fa5475896c51126e1074484b910b957c5c6578220185fc9`

```dockerfile
```

-	Layers:
	-	`sha256:aaa3fb48826b1adb2f744dc0bc1a4ec45db497eebc4ff634c13027b3cc42a6d4`  
		Last Modified: Fri, 26 Sep 2025 21:40:09 GMT  
		Size: 7.5 MB (7474366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fe9f5aa0f373bd83c4fcd310dc97e524bb1c7f72e8490ed77586885b6a48cb`  
		Last Modified: Fri, 26 Sep 2025 21:40:11 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:83967a783f30f2b65f03bf1c7be12913d28892dd68de9f5c3ad7fd225eb8e631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282880542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4342c67eed5c72502872597c60556d9b55753583727bc93cd092360435e6e93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6732308093ffadca9f5979257a664a89575a7116c201847cfc81c8d14134ab`  
		Last Modified: Fri, 26 Sep 2025 19:29:41 GMT  
		Size: 147.0 MB (147026955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465f982f215ec0de40a5796df8e4f71adbd38e25c6722a51445e6817f5e0bdb2`  
		Last Modified: Fri, 26 Sep 2025 19:29:36 GMT  
		Size: 86.5 MB (86506217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8bf7dd15a7f4d9d3e69a34416bef54887efc94c6ad05d2ee75297596a836c`  
		Last Modified: Fri, 26 Sep 2025 19:29:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a321db04a5e8d4c5263f03bac72a64bf5a40415eb2eac66c7e2169b6714d5d96`  
		Last Modified: Fri, 26 Sep 2025 19:29:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a624263b819ed359f7f866062c8840042cfa27cfd49d934e954f7bd62c22bccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce8a82b584e30f8512389857081630aabd2dec743dcc2af31c48c1553f2ec18`

```dockerfile
```

-	Layers:
	-	`sha256:472ab2957a011dbc575b0b03a8aa188f90aa7ffade1a123b92d263fc0c8293a9`  
		Last Modified: Fri, 26 Sep 2025 21:40:16 GMT  
		Size: 7.5 MB (7465869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4a000037d0cda8ba9654b11a6d4752b8766c0abacbf475be66c64eb088abdf`  
		Last Modified: Fri, 26 Sep 2025 21:40:17 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
