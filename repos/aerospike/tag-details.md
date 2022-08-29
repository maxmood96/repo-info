<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-6.0.0.5`](#aerospikece-6005)
-	[`aerospike:ee-6.0.0.5`](#aerospikeee-6005)

## `aerospike:ce-6.0.0.5`

```console
$ docker pull aerospike@sha256:6b5b0f1008549bf539e4292aa568eb9959440b61fac6712f78684b5dacc190c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-6.0.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:67eefc6dba75d1e7800bbd78bd0b9bfaf033b089dde57353b76fe2b4da38af84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120641203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8236853af7854786976c9550310f1271b6290c6f79fd115b417f5d7d9b5840e8`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 23:07:02 GMT
ENV AEROSPIKE_VERSION=6.0.0.5
# Wed, 24 Aug 2022 23:07:30 GMT
ENV AEROSPIKE_SHA256=2eb30e08fd5fa5055e328ee5e652f59efd99af66f2b9e8eede5ffb532b7bd99a
# Mon, 29 Aug 2022 18:20:13 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ];     then     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Mon, 29 Aug 2022 18:20:14 GMT
COPY file:f497c4c6974a190f79a562efd9c9c0d6b753efe43e62c3fcc2536f74ad08238d in /etc/aerospike/aerospike.template.conf 
# Mon, 29 Aug 2022 18:20:14 GMT
COPY file:fe302e12e47afe1731a34ed4ed29328c6901a3f2c9e32e307220e65cb76d53a2 in /entrypoint.sh 
# Mon, 29 Aug 2022 18:20:14 GMT
EXPOSE 3000 3001 3002
# Mon, 29 Aug 2022 18:20:14 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 29 Aug 2022 18:20:14 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298717f91f531abeb29871fc8ae073a7f1f04f690363942413552747699b6067`  
		Last Modified: Mon, 29 Aug 2022 18:21:01 GMT  
		Size: 93.5 MB (93501044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3330cf91ce75b827b745ae8dae39d275d13bd94eb9f6271173b08ece25a9c8be`  
		Last Modified: Mon, 29 Aug 2022 18:20:47 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937dd25cea4d8e3dbd980c5063020d4a6248a1a3a3e55e1a41faa59bc8d663cf`  
		Last Modified: Mon, 29 Aug 2022 18:20:47 GMT  
		Size: 810.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-6.0.0.5`

```console
$ docker pull aerospike@sha256:5b2d689c96b5d436a7ddbed684b572b136627306dd32f63fc234882b7e456264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:4ef77e1a6a748428cd4fc7a4d7cf3083613ba948d2dd45d3cb31a9feb73e4ff7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123034040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41490154c4200ab6b152d2224a8148274fe7a98dcbd046be693f5f997c636431`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Wed, 24 Aug 2022 23:07:02 GMT
ENV AEROSPIKE_VERSION=6.0.0.5
# Wed, 24 Aug 2022 23:07:02 GMT
ENV AEROSPIKE_SHA256=3b40c4aec82a93e1b2d04db47efce7d7a5f7ad29c82f66cf1d0c83775f5f4f9c
# Wed, 24 Aug 2022 23:07:03 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Mon, 29 Aug 2022 18:19:45 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;     if [ -f /usr/lib/asadm/asinfo ];     then     ln -s /usr/lib/asadm/asinfo /usr/bin/asinfo;     fi   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Mon, 29 Aug 2022 18:19:46 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Mon, 29 Aug 2022 18:19:46 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Mon, 29 Aug 2022 18:19:46 GMT
EXPOSE 3000 3001 3002
# Mon, 29 Aug 2022 18:19:46 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Mon, 29 Aug 2022 18:19:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a14d0f61e807c640a893d3ebcb1a96659e37792195f57cbaf189ceed714b7fa`  
		Last Modified: Mon, 29 Aug 2022 18:20:40 GMT  
		Size: 95.9 MB (95893825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cc95b04d74c978af01a003565b9ca5ec4d96d221a016d683b346347e22ad88`  
		Last Modified: Mon, 29 Aug 2022 18:20:26 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0dd5931f0f612eb70d0f33a7e3a4622c0a6eaf78c30432a12440cba6385c9a`  
		Last Modified: Mon, 29 Aug 2022 18:20:26 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
