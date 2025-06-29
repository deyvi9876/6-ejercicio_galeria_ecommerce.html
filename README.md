<section class="code-examples">
            <h3 style="font-size: var(--font-xl); margin-bottom: var(--space-md);">📝 Ejemplos de Implementación</h3>

            <div class="solution-hint">
                <strong>💡 Pista:</strong> Para el primer producto (smartphone), necesitas diferentes composiciones para
                móvil y desktop.
            </div>

            <h4 style="margin-bottom: var(--space-sm);">Ejemplo 1: Picture Element con Art Direction</h4>
            <div class="code-block">
                <span class="code-comment">/* Para el producto smartphone */</span>
                &lt;<span class="code-keyword">picture</span>&gt;
                <span class="code-comment">&lt;!-- Móvil: imagen cuadrada --&gt;</span>
                &lt;<span class="code-keyword">source</span>
                media="(max-width: 767px)"
                srcset="<span class="code-keyword">https://picsum.photos/400/400?random=1</span>"
                &gt;
                <span class="code-comment">&lt;!-- Desktop: imagen rectangular --&gt;</span>
                &lt;<span class="code-keyword">img</span>
                class="product-image"
                src="<span class="code-keyword">https://picsum.photos/600/400?random=1</span>"
                srcset="
                https://picsum.photos/600/400?random=1 600w,
                https://picsum.photos/1200/800?random=1 1200w
                "
                sizes="<span class="code-keyword">(max-width: 768px) 100vw, 33vw</span>"
                alt="<span class="code-keyword">Smartphone Pro Max mostrando pantalla de inicio</span>"
                loading="<span class="code-keyword">lazy</span>"
                &gt;
                &lt;/<span class="code-keyword">picture</span>&gt;
            </div>

            <h4 style="margin-bottom: var(--space-sm);">Ejemplo 2: CSS Optimizado para Imágenes</h4>
            <div class="code-block">
                <span class="code-comment">/* Estilos para contenedor de imagen */</span>
                .<span class="code-keyword">product-image-container</span> {
                aspect-ratio: <span class="code-keyword">4/3</span>; <span class="code-comment">/* Evita layout shift
                    */</span>
                overflow: <span class="code-keyword">hidden</span>;
                position: <span class="code-keyword">relative</span>;
                }

                .<span class="code-keyword">product-image</span> {
                width: <span class="code-keyword">100%</span>;
                height: <span class="code-keyword">100%</span>;
                object-fit: <span class="code-keyword">cover</span>; <span class="code-comment">/* Mantiene proporción
                    */</span>
                transition: <span class="code-keyword">transform 0.3s ease</span>;
                }

                <span class="code-comment">/* Efecto hover */</span>
                .<span class="code-keyword">product-card</span>:hover .<span class="code-keyword">product-image</span> {
                transform: <span class="code-keyword">scale(1.05)</span>;
                }
            </div>

            <div
                style="background: #e8f5e8; padding: var(--space-md); border-radius: 8px; margin-top: var(--space-md);">
                <strong>🎯 Tu Tarea:</strong>
                <ol style="margin-left: 20px; margin-top: var(--space-xs);">
                    <li>Reemplaza los placeholders con implementaciones picture/img apropiadas</li>
                    <li>Asegúrate de que cada producto use una estrategia diferente (picture, srcset, background)</li>
                    <li>Incluye lazy loading y alt text descriptivo</li>
                    <li>Testa en diferentes tamaños de ventana</li>
                </ol>
            </div>
        </section>

        // Logging para ayuda en desarrollo
        console.log(`
🚀 GUÍA PARA COMPLETAR EL EJERCICIO:

1. PRODUCTO 1 (Smartphone):
   - Usa <picture> element
   - Móvil: imagen cuadrada (mejor para scroll vertical)
   - Desktop: imagen rectangular (aprovecha espacio horizontal)

2. PRODUCTO 2 (Laptop):
   - Usa <img> con srcset y descriptores w
   - Múltiples resoluciones: 400w, 800w, 1200w
   - sizes attribute apropiado

3. PRODUCTO 3 (Auriculares):
   - Implementa formatos modernos (WebP + fallback)
   - Usa <picture> para diferentes formatos

4. PRODUCTO 4 (Smartwatch):
   - Background image responsive con CSS
   - Media queries para diferentes resoluciones

URLs de ejemplo:
- https://picsum.photos/400/400?random=X (cuadrada)
- https://picsum.photos/600/400?random=X (rectangular)
- https://picsum.photos/800/600?random=X (alta resolución)

¡Manos a la obra! 🎨
        `);

