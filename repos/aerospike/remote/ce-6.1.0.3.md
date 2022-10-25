## `aerospike:ce-6.1.0.3`

```console
$ docker pull aerospike@sha256:c36fcb31b21dbbfeeb2ad39c69106aeb341f28a4db6782e2f512b70cf6644d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.1.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:8780cf88bdb24b68315dd96d5bbc4a969fb446894a382b2ecdea3efbc8da2a0f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65141073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccb1972c1c50471966697ee799bd40597f66f5604ba8aaef30768129a72bb9d`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`
-	`SHELL`: `["\/bin\/bash","-o","pipefail","-c"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:30:28 GMT
ENV AEROSPIKE_VERSION=6.1.0.3
# Tue, 25 Oct 2022 02:30:52 GMT
ENV AEROSPIKE_SHA256=e4f9c152209547517951b78e42ca0251bd237fe1eba65b7bef81fea94ab653c9
# Tue, 25 Oct 2022 02:30:52 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 25 Oct 2022 02:30:52 GMT
SHELL [/bin/bash -o pipefail -c]
# Tue, 25 Oct 2022 02:31:07 GMT
RUN export DEBIAN_FRONTEND=noninteractive   && apt-get update -y   && apt-get install -y --no-install-recommends     apt-utils     2>&1 | grep -v "delaying package configuration"   && apt-get install -y --no-install-recommends     binutils     ca-certificates     gettext-base     wget     xz-utils   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static --progress=bar:force:noscroll -O /usr/bin/as-tini-static 2>&1   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://artifacts.aerospike.com/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian11.tgz" --progress=bar:force:noscroll -O aerospike-server.tgz 2>&1   && echo "$AEROSPIKE_SHA256 aerospike-server.tgz" | sha256sum -c -   && mkdir -p aerospike/pkg   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && ar --output aerospike/pkg -x aerospike/aerospike-tools-*.deb   && tar xf aerospike/pkg/data.tar.xz -C aerospike/pkg/   && rm -rf aerospike-server.tgz /var/lib/apt/lists/*   && dpkg -r apt-utils binutils ca-certificates wget xz-utils   && dpkg --purge apt-utils binutils ca-certificates wget xz-utils 2>&1   && apt-get purge -y   && apt-get autoremove -y   && find aerospike/pkg/opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv aerospike/pkg/etc/aerospike/astools.conf /etc/aerospike   && if [ -d 'aerospike/pkg/opt/aerospike/bin/asadm' ]; then     mv aerospike/pkg/opt/aerospike/bin/asadm /usr/lib/;     ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ]; then       ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && rm -rf /opt/aerospike/bin   && rm -rf aerospike
# Tue, 25 Oct 2022 02:31:07 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Tue, 25 Oct 2022 02:31:07 GMT
COPY file:e3973656bf47d8e3796d7b5dc7200e68dcaedc877c80f4ebeed9484f3aa315d9 in /entrypoint.sh 
# Tue, 25 Oct 2022 02:31:07 GMT
EXPOSE 3000 3001 3002
# Tue, 25 Oct 2022 02:31:07 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 25 Oct 2022 02:31:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ab0a07ad013c27e31e8d68f40c01e8d68e97a692130c638dd34e1581f761c8`  
		Last Modified: Tue, 25 Oct 2022 02:31:36 GMT  
		Size: 33.7 MB (33719228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd12014b0bb89544fd2a0bbd5eab940effd6ff29cd9177d4f7e85a591ace62a`  
		Last Modified: Tue, 25 Oct 2022 02:31:30 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb426ef8c3f7d8acef8f6b60cffe584154584ee8899424fa44270df669e74e7`  
		Last Modified: Tue, 25 Oct 2022 02:31:30 GMT  
		Size: 789.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
