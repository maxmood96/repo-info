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
