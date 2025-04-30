## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:0d0c4ebfbf0ce1731aa37cf2caf663b327688117183a91a53c9aa601110dad41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:db8fcb7256b7399cc618abdbf275107c229eddf6876d996d4d7f08b6cab88f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213096179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e074dcb820ebb3112fc39e232c25d9ab32fb1a3249922ad2fd87f3ce6d2c20ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9422688b73396143d24133eac30773a2e9e6f4d221585795e30d37d25fbf1ee`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 90.0 MB (89951979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a64b5e2c1a776b4472aa40a0830147b612722e2bb7fa4c221efd3cc2441259`  
		Last Modified: Mon, 28 Apr 2025 22:08:13 GMT  
		Size: 69.4 MB (69395423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bef49c7acdb6cce5ea5ea312d4d0cd0495ce9b207020a32e0e63f5e1460d33`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefd71d4293a37ebbf0dcdfb8ee78c2ef7a53bc28d66265e95d383c74932f7c2`  
		Last Modified: Mon, 28 Apr 2025 22:08:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01399991634a0068ecc741092a40eacf2b6d7fe0ed1ee4e80e5e30d4ccdf3a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7173015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb29250f54ca57d71da0483a5ce27ed4cc0bc86173819668c298640988b23ed8`

```dockerfile
```

-	Layers:
	-	`sha256:81d5529fc2ffbb2850f340b8ebd62e7a5ca2a548d4cdfb7784d962c54a313756`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 7.2 MB (7157201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:453d46342066fd4d828264acaafc68739d5f55c6f9357610ea266574f012ef00`  
		Last Modified: Mon, 28 Apr 2025 22:08:12 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6195d24e024ffbd9951a794b9307a7475b69a0c02f8a8bbd6c63c3fb0f0856a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210867847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaf2a9a2a44c0ca81b5fff913c07d359097cb3ab61dee9b9f4a0c8da45f5b88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea499e9a6440c89518277b243ca49b2d9515371f555e0f6fb5ae8bfd73d843e6`  
		Last Modified: Wed, 30 Apr 2025 01:51:08 GMT  
		Size: 89.1 MB (89091271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d647400935d43344d8fd0006b65eedc14a5dcfdb1a2e671ba2461d208eb2f1`  
		Last Modified: Wed, 30 Apr 2025 01:51:08 GMT  
		Size: 69.5 MB (69529557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefe9a46362a5361e8561468f5f372b043300812c3e534642560ecf59dfc2adc`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ba61a959a7027eabf5c73312b56c2171dd659a136e3d537f8ccd2541f7752`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fa870481cdd1676040743b5ca18cec97e731310a2d7e017c77d34d3bf0bca230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664eea3a1fdf305c22fe5431c8e28b318b0bf3604a2e67f9b89d9ce45491413a`

```dockerfile
```

-	Layers:
	-	`sha256:5177e8886a28200c95f920947fd42d6a6f42115021ff77c4048e7c256641dead`  
		Last Modified: Wed, 30 Apr 2025 01:51:06 GMT  
		Size: 7.2 MB (7162297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbec8d5bf03f35a246eebf0c1837ca772d79143037dc4faa51fc0c4f1a377d70`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
