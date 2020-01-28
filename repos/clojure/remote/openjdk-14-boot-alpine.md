## `clojure:openjdk-14-boot-alpine`

```console
$ docker pull clojure@sha256:14a9574741752f3ff6e53a053bf02007d3e0c012fd198696d58d85b6456eb472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:bf0956ac4b3b8bc300a527e48c937837fd3ead6f6087b4c10ab1ca7e5c9a3807
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263181326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cbd50b691cc8a95eb2f0045448f225c7f41fb586457100e5bbb2f549bcc3ef`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:15:00 GMT
ENV JAVA_HOME=/opt/openjdk-14
# Thu, 23 Jan 2020 22:15:00 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 01:03:57 GMT
ENV JAVA_VERSION=14-ea+33
# Tue, 28 Jan 2020 01:03:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/33/binaries/openjdk-14-ea+33_linux-x64-musl_bin.tar.gz
# Tue, 28 Jan 2020 01:03:58 GMT
ENV JAVA_SHA256=25344fdf7438d05166fb3471a591aacf72e5fc7ca334b59b3f90ff34ee3b27e5
# Tue, 28 Jan 2020 01:05:39 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 28 Jan 2020 01:05:39 GMT
CMD ["jshell"]
# Tue, 28 Jan 2020 02:30:18 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 28 Jan 2020 02:30:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 28 Jan 2020 02:30:18 GMT
WORKDIR /tmp
# Tue, 28 Jan 2020 02:30:20 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Tue, 28 Jan 2020 02:30:20 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 Jan 2020 02:30:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 28 Jan 2020 02:31:25 GMT
RUN boot
# Tue, 28 Jan 2020 02:31:25 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345cf19c142c73b4673b7f5195d90723d77f452a902206b91c63c6ddca4e6bb7`  
		Last Modified: Tue, 28 Jan 2020 01:09:10 GMT  
		Size: 200.4 MB (200355870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da69aa6d8bf01753acbfd1950e27df60ec278b6f7b9843994d8f255bd18a434f`  
		Last Modified: Tue, 28 Jan 2020 02:32:39 GMT  
		Size: 1.2 MB (1217237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4c124e11fa25e5008b95f4ba9d3ee878271e785be1d53190a988df8b185177`  
		Last Modified: Tue, 28 Jan 2020 02:32:43 GMT  
		Size: 58.8 MB (58821257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
