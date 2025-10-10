## `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:82c595959104ed428853316bc9abba7eb123128e62a1ad9a5cc7052e29220136
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:afa65fa849819730e81b60555eebaed3fa2b53e034c029d0a05a1f80b8b80823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274321645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e30476f6af0ac8aec7be688fe278affe4fa6ebf21033e9bc0e2e30e86855fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1aecc5533509d544cc2c1f06b8117b13e79ea03317b937b2f9022f94362ccc`  
		Last Modified: Thu, 09 Oct 2025 22:28:08 GMT  
		Size: 144.7 MB (144693289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234dd283a68a981792cbbccd2881055486c303593360a82b119e8c073ed3b346`  
		Last Modified: Thu, 09 Oct 2025 22:28:19 GMT  
		Size: 81.1 MB (81146759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b57c1852f1c5f061b2bd8d8ec5a92130d9cb906617bba8d8a0834e9cb18639d`  
		Last Modified: Thu, 09 Oct 2025 22:28:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0815254eadec4bf1f19c670747d33c3d7ea3f2bf725d4aa15a61ff48474fad5`  
		Last Modified: Thu, 09 Oct 2025 22:28:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e1f9f6bfa8c549333a1717d0de8caddaca2991abc41f91d95b9cc20bbbbc8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c574055ed12dc733f4da3001ec422dec18ca020d10e85bdbe0812fce8d0f9cc`

```dockerfile
```

-	Layers:
	-	`sha256:f71b581dad06177d823edebfd777d610918705d1857461b64373fbd5dbd9d3aa`  
		Last Modified: Fri, 10 Oct 2025 06:39:38 GMT  
		Size: 7.4 MB (7374890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e66b376dc1bc136ab0164658690ee6e7af12dc9a75facde7559328dcb5b36f6`  
		Last Modified: Fri, 10 Oct 2025 06:39:39 GMT  
		Size: 15.8 KB (15819 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c743c40e38d294659648add1c3ffed43ebf746d59cd61bfd1d387e621bf0d569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272932154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9634b25d98e96956a2e0581f54b8fdfeec5d806fe4df01e9108607d5752bafdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc98c6859fb2cff6c69a719e2710ceeb970a5729bde947595de50b88a0127d5`  
		Last Modified: Fri, 10 Oct 2025 06:45:32 GMT  
		Size: 143.5 MB (143542159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209f7d664abd0636898640b8ed2c79872f5a136bf6fd33953cf82d02f2cb8dbf`  
		Last Modified: Fri, 10 Oct 2025 03:56:08 GMT  
		Size: 81.0 MB (81030038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46114242384291fd7ba82644c9d877f406c01a4cebefcdba464e91c62fea063b`  
		Last Modified: Thu, 09 Oct 2025 22:32:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52c87def21084ed0090f9a433e3b7011286a60d3ef9070ee573f44f34eea436`  
		Last Modified: Thu, 09 Oct 2025 22:33:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:300bcc6f2d5625589c4549644a56cbd1d69238f264000815177df57ee63127e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b015ff9267e5b85428e16c764ebc0683c2b7a94a65a5fa7623705e761c126c5b`

```dockerfile
```

-	Layers:
	-	`sha256:dea2ffc322095161f175119e7bcf75e8170a358175c354f85ec63a8b5eff3d8c`  
		Last Modified: Fri, 10 Oct 2025 06:39:44 GMT  
		Size: 7.4 MB (7380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8ed233539ec5635b48213562aaeb51e99740dc5a34ef9367bdf9f805ab8e4f4`  
		Last Modified: Fri, 10 Oct 2025 06:39:45 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:df506dd92b82479529396dac49a3d4fc84cadf044388c4c7394a0c71f4ee86ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283686316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dde72f7e34c9c4bfa398ab3c033cab5df07d0c5a817b911df19750a0eb6f94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e75ea4489e91030cf1e37f530c1fe9cc693e3ab296c65e9adb60b605fc10f`  
		Last Modified: Fri, 10 Oct 2025 05:15:59 GMT  
		Size: 144.4 MB (144372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd14004106c6ebf3b8e6b9e3ee627103fc849a673f020136fc44b854ef376ee0`  
		Last Modified: Fri, 10 Oct 2025 05:25:23 GMT  
		Size: 87.0 MB (86985616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd25e7f98f2062018156e49bd6da1bd1b781a40f17dcb8163818620ab3429908`  
		Last Modified: Fri, 10 Oct 2025 05:25:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb827d628afe12ce8120790a435b8abd9cc92b16c0b8ed88b6b5dc123494e70d`  
		Last Modified: Fri, 10 Oct 2025 05:25:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52a5201e922826fbab9bbef92c5b81bec9422b1d3ae3038873423e43df55ac29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641e1d2eadd903ea5e97f46f6b94558f60f4a97773bdac795a18ef13c62a8617`

```dockerfile
```

-	Layers:
	-	`sha256:91295869b8745d3628ef339249e6bd0ad9b8c1c2a53bed81118b9d63122643fd`  
		Last Modified: Fri, 10 Oct 2025 06:39:50 GMT  
		Size: 7.4 MB (7380104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7c805831dd009b7ef63492a71835bf0cef7ca6e1145c2e8d1f637533344214`  
		Last Modified: Fri, 10 Oct 2025 06:39:51 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fa892e42e8101d9f9961b6a8681a89aa325ec7f15adffc8439dfd49109e2e6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261818655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acede584f06e6ce66a23a3f53001c78d92df1db6e1d7d5261e351293e6ef3dc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afa8bb81ce30bcf13eb0db5dbd6d2b5add61080756bc490e8e5412b5d8260`  
		Last Modified: Thu, 09 Oct 2025 23:08:30 GMT  
		Size: 134.7 MB (134723624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa8c44b70e05464954399a13069cc93c9310bd31a40a0e50376ea20db89174`  
		Last Modified: Thu, 09 Oct 2025 23:14:21 GMT  
		Size: 80.0 MB (79956545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54a9b659d7b6b86fb1a86d7a709880f72dc18d00a87406a7ad8ccc05f087491`  
		Last Modified: Thu, 09 Oct 2025 23:14:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668704c839bb49aa0df365047ddef5c2467945903c874806c774cf0f41c15244`  
		Last Modified: Thu, 09 Oct 2025 23:14:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1ce04a443e15874923b448dde2edbec12cacc9d4ea00258799262767e0d10efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea6a3f8492569151287ec59a26407862e08d4607a6ade807be5ba7f3f88e070`

```dockerfile
```

-	Layers:
	-	`sha256:97de74b909dbc06e400809c6cd0bb4e6c6a4f4f80981d2ede6f9b948b6c9e005`  
		Last Modified: Fri, 10 Oct 2025 00:37:11 GMT  
		Size: 7.4 MB (7366209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ad56b4b0ae2c5847eb87da3652ce00182701e6e185400b2295ba38f52f6217`  
		Last Modified: Fri, 10 Oct 2025 00:37:12 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
