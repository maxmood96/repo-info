## `cirros:latest`

```console
$ docker pull cirros@sha256:4e8ac7a10251079ad68188b1aab16f6e94d8708d82d0602953c43ad48c2f08ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `cirros:latest` - linux; amd64

```console
$ docker pull cirros@sha256:483f15ac97d03dc3d4dcf79cf71ded2e099cf76c340f3fdd0b3670a40a198a22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5953672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cae1daf5f682cb6403a766b3e6afd73a102296910f27ea1ec392b54dc0c188`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:36:43 GMT
ADD file:bf4d7c23fe6b77a5c46f4c3ece606130b86aa04af3fbb2a320fb4a4d412c4603 in / 
# Mon, 08 Mar 2021 21:36:44 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:36:45 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:36:45 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:d0b405be7a3253cffc2d4b8425dd78c06d4196846dfe4d8fe45935f8d30fa351`  
		Last Modified: Mon, 08 Mar 2021 21:36:59 GMT  
		Size: 6.0 MB (5952271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd054094a03766a7be2860c487e0752bd99b1a636e189a2f9f2a29af58f2814e`  
		Last Modified: Mon, 08 Mar 2021 21:36:59 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a00de1ec8ac5311a5d4166e3433bb59659057b5be4de6465234975bec50742`  
		Last Modified: Mon, 08 Mar 2021 21:36:56 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; arm variant v5

```console
$ docker pull cirros@sha256:ed85547a3a12b37572d313f04e6e31825651de9f0479308983ddf16bfba137be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5634245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d2544786bb39abf1eb7b059b2ccea8ef91e3c77063a0db4b2b74c0b12076b8`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:51:02 GMT
ADD file:d452db6e53e5ba209c771ecfc8acc0e1991f018f8578e48e0d0dce69e46395b9 in / 
# Mon, 08 Mar 2021 21:51:07 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:51:11 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:51:11 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:231303b903e38cc8d918f588a01a3320b9fb4b4c95fa20f9852b95624c251df9`  
		Last Modified: Mon, 08 Mar 2021 21:51:37 GMT  
		Size: 5.6 MB (5632836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13f5ceef94fa1980f13a29a1d7f1400527bc0f8d23b2f22b1c17de1bf4171ca`  
		Last Modified: Mon, 08 Mar 2021 21:51:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b47ac554ba1058e0f116cd29b5480550dcb1afed47f798252cdc224a5ba2f8`  
		Last Modified: Mon, 08 Mar 2021 21:51:34 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; arm64 variant v8

```console
$ docker pull cirros@sha256:b0ec901435d6335a85b3e006ab78249678c4fc07d8b88d40b861b874a6c57d84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386fdcd60643778716b35204149f94e4bf2e0de7e26d06ff7b44d88d0a8b9f0a`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:43:00 GMT
ADD file:7f294f3d60585f86a27be204f949a663c79c9187a153fe00b725e8fa062cf493 in / 
# Mon, 08 Mar 2021 21:43:03 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:43:05 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:43:06 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:e6a197a3618a47fbe537101b254c366a779102387d42cf6a37a38f61534ab352`  
		Last Modified: Mon, 08 Mar 2021 21:43:20 GMT  
		Size: 5.4 MB (5380157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68e3274d10a80782e64941f22cfe57491bed55fc8bd3fd3f305f3d8ad8df009`  
		Last Modified: Mon, 08 Mar 2021 21:43:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e38f2754882d4495b5338215d4e23127ee0041eef571cdcfc2b4ff53c16a24`  
		Last Modified: Mon, 08 Mar 2021 21:43:19 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; 386

```console
$ docker pull cirros@sha256:111dd6cf830531a11fe07cede5845cb0c6f020171e485f2f1b3342714b99bcaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5531817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb487fd3a0f68afa6592346edf47ea792e2bfdb0367455103ee21c9e8e3b91f`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 22:01:41 GMT
ADD file:6fe295a0acec8cf81b2eb7b6868ad7e913a4b8d73574bdacba578b3d05d4f2d5 in / 
# Mon, 08 Mar 2021 22:01:42 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 22:01:43 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 22:01:43 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:6ec03cf697719ca502eb22d6de2bc3d696c52a6ba02d190332a1f21e542e048d`  
		Last Modified: Mon, 08 Mar 2021 22:02:01 GMT  
		Size: 5.5 MB (5530412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f1cfcdb21741b197e2bc5bf26ca7b0f5792f154130c3f88b26e44b50e57d07`  
		Last Modified: Mon, 08 Mar 2021 22:02:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14a0418e0a405f9acd1059962a1d26ca670fb5a4b764969ba3995282615d461`  
		Last Modified: Mon, 08 Mar 2021 22:02:00 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `cirros:latest` - linux; ppc64le

```console
$ docker pull cirros@sha256:d73c78dc6c4a275c6cb1bf46654ede0305b76b430a8cb3e9d114315c1f4d2ad1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5770839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93df8c5c52071e4dd5e2ca046f7d33481ea590317b92611c992dc101cf9f9b2c`
-	Default Command: `["\/sbin\/init"]`

```dockerfile
# Mon, 08 Mar 2021 21:33:05 GMT
ADD file:37ce090900e2d750646c4d7da4fbb79559e30b5b817c833396c86613236ba838 in / 
# Mon, 08 Mar 2021 21:33:21 GMT
RUN rm /etc/rc3.d/S40-network
# Mon, 08 Mar 2021 21:33:33 GMT
RUN sed -i '/is_lxc && lxc_netdown/d' /etc/init.d/rc.sysinit
# Mon, 08 Mar 2021 21:33:39 GMT
CMD ["/sbin/init"]
```

-	Layers:
	-	`sha256:587c91809a2ae1af15d948969c3a1adb2aad2dbe2cbb6a2b8982a5cf9d14c7ef`  
		Last Modified: Mon, 08 Mar 2021 21:34:03 GMT  
		Size: 5.8 MB (5769433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01739d1b3e0963fe3d0194afd70a85c6098f0139dff49965d2ce40342d33de96`  
		Last Modified: Mon, 08 Mar 2021 21:34:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2169930d58d52208fd25b17049537fa4ec9192f04fc372a1cb57a20d7a8d3fd`  
		Last Modified: Mon, 08 Mar 2021 21:34:01 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
