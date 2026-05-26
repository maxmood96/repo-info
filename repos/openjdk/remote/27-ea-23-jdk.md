## `openjdk:27-ea-23-jdk`

```console
$ docker pull openjdk@sha256:4d7ef67068400a50e6081c062af20f4aaaa574915206bc62bf5a931fc1608c18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-23-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:ddf1c6bb343ea49109de9a8052fd6769ed068facabb409a93cc25a9483cb8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309561614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27947fa2d888c704c259fbc8e983232edb54fd8a8ffa5e33db8382a2367353bb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:08:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 26 May 2026 19:08:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 26 May 2026 19:08:19 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:08:19 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:08:19 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:08:19 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:08:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bf7577febee2eb5463e858b1308a2d14fadbbdad30d9cf809c7f0d64245e8d`  
		Last Modified: Tue, 26 May 2026 19:08:40 GMT  
		Size: 37.7 MB (37688122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329217fb40e70c44de73df02de3295e2e0fa1c6c18a8ae04d52c07f8ed6e18be`  
		Last Modified: Tue, 26 May 2026 19:08:46 GMT  
		Size: 228.8 MB (228792910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:ddc7dd8693cdf55c49489bf1661e6068495a058d9a404c0e468258d92da99d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cd246af24acb9168686beffe84490d48085b24cfbafa838be5ef667f3c80e1`

```dockerfile
```

-	Layers:
	-	`sha256:7412335a6272ef636e8caf7f68c47ef69e1ef390340fb304f87d98b92b64a271`  
		Last Modified: Tue, 26 May 2026 19:08:38 GMT  
		Size: 2.4 MB (2367747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e70f68d9566b3b1c5c2e323695f1a26c5ee00497edefdc468a0a5a52771ea5f`  
		Last Modified: Tue, 26 May 2026 19:08:38 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-23-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:782d9223d549c95bd13d999436d24bfe53c08a2db4c8d9ec36f0e727e6756fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305955314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8f9c48681fc9715930afb8c433c57b0306a34b9d6857166ea5118ac189621`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 19:10:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 26 May 2026 19:10:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 26 May 2026 19:10:52 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 19:10:52 GMT
ENV LANG=C.UTF-8
# Tue, 26 May 2026 19:10:52 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:10:52 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='b7ef4c5d5b31b1da3d1ffaa1101173333c25937f5db7d8b150e7b8a20bd70cb7'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='fc322d442a40de5c1b80f1d8340212c8945e424693fca39a8006accd3427bf59'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 26 May 2026 19:10:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ff3593a9f7badd969f2351d12f0602df5397d48593dd6e3505642689ff19df`  
		Last Modified: Tue, 26 May 2026 19:11:15 GMT  
		Size: 37.7 MB (37696071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18ed9669941852be28307f50895ca2c21b80c98a8edeec9b5f1551dec1e45f9`  
		Last Modified: Tue, 26 May 2026 19:11:18 GMT  
		Size: 226.8 MB (226763548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-23-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:93d993ac67702fcd341133722e959034585f2b9bbbc05e89422c826e72544d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1457c184c5eed6322cc524ffc08fbca8e811ca15773b92a99c6ba5e02a86a41`

```dockerfile
```

-	Layers:
	-	`sha256:f829613a2ff10657f0c31ad2c6982299e379421507299f9d7ef52e3325c13d9e`  
		Last Modified: Tue, 26 May 2026 19:11:13 GMT  
		Size: 2.4 MB (2367275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7da3b16fabe506f79b39a17f3290dca105b10afcbe7f8750c1d6d9d1f9b54124`  
		Last Modified: Tue, 26 May 2026 19:11:13 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-23-jdk` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:79bafb23ebe47335dccae88025085a2a371709d63bc2e80de78ddffdee88ddcc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2431959630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434e8029e744d1b45ae167e298c22171a3a840d982cc8545c6212a5b0bb3e18d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 26 May 2026 19:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2026 19:15:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:15:26 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 26 May 2026 19:15:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:15:34 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:15:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_windows-x64_bin.zip
# Tue, 26 May 2026 19:15:37 GMT
ENV JAVA_SHA256=7a3570aa872e47b54f71fd9c142dc466b4b796ffc20ebd57cd26987efab6546f
# Tue, 26 May 2026 19:16:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 26 May 2026 19:16:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bba8ce69ea3c2c1dc61eae975c3e5c01e5eba038c6953ebd7963198d5be4b20`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b8c6ba57244681d379c4e2a8b443adfad61fcaa045e7594b9661eda1c21b2e`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 389.2 KB (389197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc9692fc6d3e3d2c1d0dc84e33efe2f0b6abc274f699552d11375f7c7145ee2`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa33a9c9981bb572e7bf646475288620d1074a459c165d6d3009b60d67d01383`  
		Last Modified: Tue, 26 May 2026 19:16:58 GMT  
		Size: 334.3 KB (334334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632607d87c51351820c3bf690e22b92de568c94a8c05ac9cf20dc96a5e3a1050`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb9f5cdb504b31e895d83e88994a029fcfd38f1e3f0533849da3d56603662dc`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65733d780f40e4633347e4446fc3cd4fdd4d5af07d8a142cda947beb5f2f3399`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d47509ed73e207b30fdfbb8ab42305a200f8c192e5744afe69cb94f60ca1f7b`  
		Last Modified: Tue, 26 May 2026 19:17:10 GMT  
		Size: 225.3 MB (225286467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08272f4e9cff37ef4682f1dd138e35af5bf17b5d5dd360042129636b115ee46`  
		Last Modified: Tue, 26 May 2026 19:16:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-23-jdk` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:5b09bae3df6c7ef2ec5419e26fdaabeb707b177e57d2ef6332cf416c1a087116
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348528572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf92ca682d8d4821c84ab5652c69e87648dadfde6beee6d13703acda1b13d99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 26 May 2026 19:18:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2026 19:19:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:19:39 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 26 May 2026 19:19:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:19:48 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:19:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_windows-x64_bin.zip
# Tue, 26 May 2026 19:19:50 GMT
ENV JAVA_SHA256=7a3570aa872e47b54f71fd9c142dc466b4b796ffc20ebd57cd26987efab6546f
# Tue, 26 May 2026 19:21:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 26 May 2026 19:21:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f74e31a73ad89127e60143561d9ad3841162a75b2db137fded34c76e7ce6180`  
		Last Modified: Tue, 26 May 2026 19:21:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c978d99f9d2ebbd2bcebb897c7a0836352eeb83a21a39101a03ce296ea6868`  
		Last Modified: Tue, 26 May 2026 19:21:53 GMT  
		Size: 514.0 KB (514011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e05ee2bf302da902b7dc3a8557b0c24d9cfc86a2337bb0f9ab7db6b578b97e`  
		Last Modified: Tue, 26 May 2026 19:21:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def4c72472d0d1bf20cfca18565f32a020f15bd04adda548d44feb50dfc6f8b1`  
		Last Modified: Tue, 26 May 2026 19:21:52 GMT  
		Size: 314.2 KB (314221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4f56301d3599e9fedfebc462669f428531ef54991adc24df444a8abf0c782`  
		Last Modified: Tue, 26 May 2026 19:21:50 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd6e494f9dbb19dddf83893322b6b7000485e175c2edfe42dfd2f81e1d19b69`  
		Last Modified: Tue, 26 May 2026 19:21:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4b6212ee50cedd4a472cc1b3ac00ce7f25a4a1b1c1cbbbaa1d60303f28caf5`  
		Last Modified: Tue, 26 May 2026 19:21:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f31200730fbf78f26528841a93e8256d226a8d3f6d6d016549a956e1a854dd`  
		Last Modified: Tue, 26 May 2026 19:22:05 GMT  
		Size: 225.3 MB (225271918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878a0fd2108acf4588dd354a30af5a7106b4f4e85dbc7ac60fb92024d8fce1f`  
		Last Modified: Tue, 26 May 2026 19:21:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
