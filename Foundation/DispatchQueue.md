# Foundation | DispatchQueue

DispatchQueue manages the execution of work items. Each work item submitted to a queue is processed on a pool of threads managed by the system.

```typescript

/**
 * Returns main queue. 
 */
static readonly main: DispatchQueue

/**
 * Returns global queue. 
 */
static readonly global: DispatchQueue

/**
 * Creates an instance with specific identifier optionally. 
 */
constructor(identifier?: string): DispatchQueue

/**
 * create an async task.
 */
async(asyncBlock: () => void): void

/**
 * create an async task after seconds delay.
 */
asyncAfter(delayInSeconds: number, asyncBlock: () => void): void

/**
 * create an isolate task.
 */
isolate(isolateBlock: () => void, ...arguments): void

```
